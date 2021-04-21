## Getting Started

To get started when developing one of our Dockerfile projects (after you have installed the requirements mentioned above), the first command you need to run in the root of the project is:

```
npm i
```

This will set up a pre-commit hook that will automatically lint your commits before committing. It will also refresh the repository to include the latest configurations. This ensures that other developers are using the same project code as you.

### Descriptions of Build Scripts

After you run `npm i`, you can view the various build commands by running `npm run info`. This will display a chart in your terminal with descriptions of the build scripts. It might look something like this:

```shell
❯ npm run info

> dockerfile-project@0.0.1 info
> npm-scripts-info

build:
  Build the Docker image on the local machine
build:slim:
  Build a slim Docker image with Dockerslim
commit:
  The preferred way of running git commit (instead of git commit, we prefer running 'npm run commit')
info:
  Logs descriptions of all the npm tasks
fix:
  Automatically fix formatting errors
prepare-release:
  Updates the CHANGELOG with commits made using 'npm run commit' and updates the project to be ready for release
shell:
  Run the Dockerfile and open its shell
test:
  Validates the Dockerfile and performs project linting
update:
  Runs .update.sh to automatically update meta files and documentation
version:
  Used by 'npm run prepare-release' to update the CHANGELOG and app version
```

You can then build the Docker image, for instance, by running `npm run build`. You can check out exactly what each command does by looking at the `package.json` file in the root of the project.

### Creating Dockerslim Builds

Whenever possible, a Dockerslim build should be provided and tagged as `:slim`. Dockerslim provides many configuration options so please check out the [Dockerslim documentation]({{ website.dockerslim_github_page }}) to get a thorough understanding of it and what it is capable of. When you have formulated *and fully tested* the proper Dockerslim configuration, you can add it to the `package.json` next to the option that says `"build:slim"`.
