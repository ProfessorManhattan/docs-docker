## Getting Started

To get started when developing one of [our Dockerfile projects]({{ repository.group.dockerfile }}) (after you have installed [Docker]({{ repository.project.docker }})), the first command you need to run in the root of the project is:

```shell
bash .start.sh
```

This command will:

* Install missing dependencies without sudo (i.e. the binary dependencies will be stored in `~/.local/bin` and your PATH will be updated to reference the `~/.local/bin` directory)
* Ensure Node.js dependencies are installed if the `node_modules/` folder is missing
* Copy (and possibly overwrite) the shared common files from the [Dockerfile common files repository]({{ repository.project.common_docker }}) and the [shared common files repository]({{ repository.project.common_shared }})
* Update the `package.json` file
* Re-generate the documentation
* Register a pre-commit hook that only allows commits to register if tests are passed

### Descriptions of Build Scripts

After you run `npm i` (or `bash .start.sh`), you can view the various build commands by running `npm run info`. This will display a chart in your terminal with descriptions of the build scripts. It might look something like this:

```shell
❯ npm run info

> ansible-lint@0.0.23 info
> npm-scripts-info

build:
  Build the regular Docker image and then build the slim image
build:latest:
  Build the regular Docker image
build:slim:
  Build a compact Docker image with DockerSlim
commit:
  The preferred way of running git commit (instead of git commit, we prefer you run 'npm run commit' in the root of this repository)
fix:
  Automatically fix formatting errors
info:
  Logs descriptions of all the npm tasks
prepare-release:
  Updates the CHANGELOG with commits made using 'npm run commit' and updates the project to be ready for release
publish:
  Creates new release(s) and uploads the release(s) to DockerHub
scan:
  Scans images for vulnerabilities
shell:
  Run the Docker container and open a shell
sizes:
  List the sizes of the Docker images on the system
test:
  Validates the Dockerfile, tests the Docker image, and performs project linting
update:
  Runs .start.sh to automatically update meta files and documentation
version:
  Used by 'npm run prepare-release' to update the CHANGELOG and app version
start:
  Kickstart the application
```

You can then build the Docker image, for instance, by running `npm run build` or list the sizes of Docker images on your system by running `npm run sizes`. You can check out exactly what each command does by looking at the `package.json` file in the root of the project.

### Creating DockerSlim Builds

Whenever possible, a DockerSlim build should be provided and tagged as `:slim`. DockerSlim provides many configuration options so please check out the [DockerSlim documentation]({{ website.dockerslim_github_page }}) to get a thorough understanding of it and what it is capable of. When you have formulated *and fully tested* the proper DockerSlim configuration, you can add it to the `.blueprint.json` file.

### Updating the `.blueprint.json` File

The `.blueprint.json` file stores some of the information required to automatically generate, scaffold, and update this repository when `bash .start.sh` is run. When creating a new Dockerfile project, the `.blueprint.json` file must be filled out. The following chart details the possible data that you can populate `.blueprint.json` with:

{{ blueprint_variables }}

When populating the `.blueprint.json` file, it is a good idea to check out [repositories in the same group]({{ repository.group.dockerfile }}/{{ subgroup }}) to see what variables are being utilized.

## Creating a New Dockerfile Project

If you are creating a new Dockerfile project, you should first populate the `.blueprint.json` file as described above. After you have a `.blueprint.json` in the root of the project, you should also copy the `.start.sh` file from another one of our Dockerfile projects. With the files in place, you can then run `bash .start.sh`. This will copy over all the other files and set up the project. You should then:

1. Rename the `"name"` field to the desired image name (e.g. `megabytelabs/**name**:slim`).
2. Code your Dockerfile
3. Create a test case for your Dockerfile (more details are in the [Creating Test Cases](#creating-test-cases) section)
4. Test your Dockerfile by running `npm run test`
5. Build your Dockerfile after you finish coding it using `npm run build`
6. After everything is completely done, test the complete flow by running `npm run publish`
