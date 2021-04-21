## Example Usage

Without having to clone this repository, you can pull the latest Dockerfile to have the image cached locally by running:

```
docker pull megabytelabs/{{ pkg.name }}:latest
```

### Building the Docker Container

You can modify this Dockerfile to suit your purposes. After you make changes to the Dockerfile, you can upload your custom container to [Docker Hub]({{ website.dockerhub }}) using the following code:

```
docker login -u "DOCKERHUB_USERNAME" -p "DOCKERHUB_PASSWORD" docker.io
docker build --pull -t "DOCKERHUB_USERNAME/{{ pkg.name }}:latest" .
docker push "DOCKERHUB_USERNAME/{{ pkg.name }}:latest"
```

Replace DOCKERHUB_USERNAME and DOCKERHUB_PASSWORD in the snippet above with your Docker Hub username and password. The commands will build the Docker image and upload it to Docker Hub. You can see this logic being implemented as a [GitLab CI task here]({{ repository.link.dockerhub_ci_task }}). This GitLab CI task works in conjunction with the `.gitlab-ci.yml` file in the root of this repository. By taking these extra steps, you can save yourself time by letting GitLab build and publish your images everytime you push to your master branch.

### Build Tools

You might notice that we have a lot of extra files considering that this repository basically boils down to a single Dockerfile. These extra files are meant to make team development easier, predictable, and enjoyable. If you have a recent version of [Node.js]({{ repository.project.node }}) installed, you can get started using our build tools by running `npm i` in the root of this repository. After that, you can run `npm run info` to see a list of the available development features. For more details, check out the [CONTRIBUTING.md]({{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}/-/blob/master/CONTRIBUTING.md) file.
