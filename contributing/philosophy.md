## Philosophy

When you are working on one of our Dockerfile projects, try asking yourself, "How can this be improved?" By asking yourself that question, you might decide to take the project a step further by opening a merge request that:

* Reduces the size of the Docker container by converting it from a Ubuntu image to an Alpine image
* Improves the security and reduces the size of the Docker container by including a configuration for providing a Dockerslim build
* Linting the Dockerfile to conform with standards set in place by [Haskell Dockerfile Linter]({{ repository.group.ansible_roles}}/hadolint)

All of these improvements would be greatly appreciated by us and our community. After all, we want all of our Dockerfiles to be the best at what they do.
