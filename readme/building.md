### Building the Docker Container

You can modify this Dockerfile to suit your purposes. After you make changes to the Dockerfile, you can upload your custom container to [Docker Hub]({{ website.dockerhub }}) using the following code:

```shell
docker login -u "DOCKERHUB_USERNAME" -p "DOCKERHUB_PASSWORD" docker.io
docker build --pull -t "DOCKERHUB_USERNAME/{{ pkg.name }}:latest" .
docker push "DOCKERHUB_USERNAME/{{ pkg.name }}:latest"
```

Replace DOCKERHUB_USERNAME and DOCKERHUB_PASSWORD in the snippet above with your Docker Hub username and password. The commands will build the Docker image and upload it to [Docker Hub](https://hub.docker.com/) where it will be publicly accessible. You can see this logic being implemented as a [GitLab CI task here]({{ repository.link.dockerhub_ci_task }}). This GitLab CI task works in conjunction with the `.gitlab-ci.yml` file in the root of this repository.
