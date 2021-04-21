## Testing

Testing is an **extremely important** part of contributing to this project. Before opening a merge request, **you must test all common use cases of the Docker container**. This should be relatively straight-forward.

### Testing Dockerslim Builds

It is especially important to test Dockerslim builds. Dockerslim works by removing all the components in a container's operating system that it thinks are unnecessary. This can easily break things.

For example, if you are testing a Dockerslim build that packages [ansible-lint]({{ repository.project.ansiblelint }}) into a slim container, you might be tempted to simply test it by running `docker exec -it MySlimAnsibleLint ansible-lint`. This will ensure that the ansible-lint command can be accessed but that is not enough. You should also test it by passing in files as a volume and command line arguments. It is **important** to test all common use cases. Some people might be using the ansible-lint container in CI where the files are injected into the Docker container and some people might be using an inline command to directly access anible-lint from the host.

### Testing Web Apps

When testing Docker-based web applications, ensure that after you destroy the container you can bring the Docker container back up to its previous state using volumes and file mounts. This allows users to periodically update the Docker container while having their settings persist.
