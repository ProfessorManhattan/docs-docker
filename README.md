# Dockerfile Documentation

This repository contains documentation partials written in Markdown used for generating the documentation for our various Dockerfile repositories.

You can rebuild the documentation by running the following command in the parent repository's root folder:

```shell
bash .update.sh
```

Whenever master is updated in this repository, GitLab CI will propagate the changes to all the relevant projects. This is done by setting an environment variable named DOWNSTREAM_GROUP_IDS equal to a comma seperated list of subgroups with projects that should all be updated.
