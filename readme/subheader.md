<h4>
  <a href="{{ website.homepage }}" title="Megabyte Labs homepage">
    <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/home.svg" />
  </a>
  <a href="{{ profile.dockerhub }}" title="Megabyte Labs profile on DockerHub">
    <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/dockerhub-profile.svg" />
  </a>
  <a href="{{ website.dockerhub_repository }}/{{ slug }}" title="DockerHub page for this project">
    <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/dockerhub-image.svg" />
  </a>
  <a href="{{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}/-/blob/master/CONTRIBUTING.md" title="Find out how to contribute to this project">
    <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/contribute.svg" />
  </a>
  <a href="{{ chat_url }}" title="Slack chat room">
    <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/chat.svg" />
  </a>
  <a href="{{ profile.github }}/docker-{{ slug }}" title="GitHub mirror">
    <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/github.svg" />
  </a>
  <a href="{{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}" title="GitLab repository">
    <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/gitlab.svg" />
  </a>
</h4>
<p>
  <a href="{{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}">
    <img alt="Version" src="https://img.shields.io/docker/v/megabytelabs/{{ slug }}?logo=docker&logoColor=white&style={{ badge_style }}" />
  </a>
  <a href="https://hub.docker.com/repository/docker/megabytelabs/{{ slug }}">
    <img alt="DockerHub image size: {{ pretty_name }}" src="https://img.shields.io/docker/image-size/megabytelabs/{{ slug }}?logo=docker&logoColor=white&style={{ badge_style }}">
  </a>
  <a href="https://hub.docker.com/repository/docker/megabytelabs/{{ slug }}" target="_blank">
    <img alt="DockerHub pulls: {{ pretty_name }}" src="https://img.shields.io/docker/pulls/megabytelabs/{{ slug }}?logo=docker&logoColor=white&style={{ badge_style }}" />
  </a>
  <a href="{{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}" target="_blank">
    <img alt="GitLab pipeline status" src="https://gitlab.com/megabyte-labs/dockerfile/{{ subgroup }}/{{ slug }}/badges/master/pipeline.svg?style={{ badge_style }}" />
  </a>
  <a href="{{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}/-/raw/master/LICENSE" target="_blank">
    <img alt="License: {{ license }}" src="https://img.shields.io/badge/License-{{ license }}-yellow.svg?style={{ badge_style }}" />
  </a>
  <a href="{{ profile.github }}" target="_blank">
    <img alt="GitHub: {{ profile.github }}" src="https://img.shields.io/github/followers/MegabyteLabs?style=social" target="_blank" />
  </a>
  <a href="https://twitter.com/{{ profile.twitter }}" target="_blank">
    <img alt="Twitter: {{ profile.twitter }}" src="https://img.shields.io/twitter/url/https/twitter.com/{{ profile.twitter }}.svg?style=social&label=Follow%20%40{{ profile.twitter }}" />
  </a>
</p>
