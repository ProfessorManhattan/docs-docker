## Example Usage

Without having to clone this repository, you can pull the latest Dockerfile to have the image cached locally by running:

```shell
docker pull megabytelabs/{{ pkg.name }}:latest
```

### Experimenting / Shelling Into Container

Although this image is intended to be used with Ansible Molecule (which is described below), you can start the container and shell into it by running the following commands if you are curious:

```shell
docker run megabytelabs/{{ pkg.name }}:latest
docker exec -it megabytelabs/{{ pkg.name }}:latest /bin/bash
```

Note that after you exit from the shell session, the container will still be running. After you are done experimenting with the container, you can destroy it by running:

```shell
docker ps -a     # Copy the ID of the image you wish to delete
docker rm <ID>
```

Alternatively, you can shell into the container and have Docker automatically remove the container when you exit by running:

```shell
docker run -it --rm megabytelabs/{{ pkg.name }}:latest /bin/sh
```