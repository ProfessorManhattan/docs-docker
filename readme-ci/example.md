## Example Usage

There are several different ways you can use the Docker container provided by this project. For starters, you can test the feature out locally by running:

```shell
docker run -v ${PWD}:/work -w /work megabytelabs/{{ pkg.name }} {{ docker_command }}
```

This allows you to run {{ pretty_name }} without installing it locally. This could be good for security and also keeps your file system clean. You can also add a bash alias to your `~/.bashrc` file so that you can run the {{ pretty_name }} command at any time. To do this, add the following snippet to your `~/.bashrc` file (or equivalent):

```shell
{{ docker_command }}() {
    docker run -v ${PWD}:/work -w /work megabytelabs/{{ pkg.name }}:{{ preferred_tag }} {{ docker_command }}
}
```

### Integrating with GitLab CI

The main purpose of this project is to build a Docker container that can be used in CI pipelines. If you want to incorporate this CI pipeline tool into GitLab CI project then your first step would be to create a `.gitlab-ci.yml` file in the root of your repository that is hosted by GitLab. Your `.gitlab-ci.yml` file should look something like this:

```yaml
---
stages:
  - lint

include:
  - remote: https://gitlab.com/megabyte-space/gitlab-ci-templates/-/raw/master/{{ slug }}.gitlab-ci.yml
```

That is it! {{ pretty_name }} will now run anytime you commit code (that matches the parameters laid out in the `remote:` file above). Ideally, for production, you should copy the source code from the `remote:` link above to another location and update the `remote:` link to the file's new location. That way you do not have to worry about any changes that are made to the `remote:` file by our team.
