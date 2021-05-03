### Building a Slim Container

Some of our repositories support creating a slim build via [DockerSlim](https://gitlab.com/megabyte-labs/ansible-roles/dockerslim). According to [DockerSlim's GitHub page](https://github.com/docker-slim/docker-slim), slimming down containers reduces the final image size and improves the security of the image by reducing the attack surface. It makes sense to create a slim build for anything that supports it, including Alpine images. On their GitHub page, they report that some images can be reduced in size by up to 448.76X. This means that if your image is naturally 700MB then it can be reduced to 1.56MB! It works by removing everything that is unnecessary in the container image.

As a convenience feature, we include a command defined in `package.json` that should build the slim image. Just run `npm run build:slim` after running `npm i` (with [Node.js >9](https://gitlab.com/megabyte-labs/ansible-roles/nodejs) installed) in the root of this repository to build a slim build.

To build and publish a slim Dockerfile to Docker Hub, you can use the following as a starting point:

```shell
docker login -u "DOCKERHUB_USERNAME" -p "DOCKERHUB_PASSWORD" docker.io
DOCKER_SLIM_BUILD_COMMAND
docker push "DOCKERHUB_USERNAME/{{ pkg.name }}:slim"
```

It might even be possible to modify the DockerSlim command above to reduce the footprint even more than our command. If you come up with an improvement, please do [open a pull request]({{ repository.group.dockerfile_ci}}/{{ slug }}/-/issues/new). And again, make sure you replace DOCKERHUB_USERNAME and DOCKERHUB_PASSWORD in the snippet above with your Docker Hub username and password. The commands will build the Docker image and upload it to [Docker Hub](https://hub.docker.com/) where it will be publicly accessible. You can see this logic being implemented as a [GitLab CI task here]({{ repository.link.dockerhub_ci_task_slim }}).