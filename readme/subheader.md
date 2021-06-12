<div align="center">
  <h4 align="center">
    <a href="{{ website.homepage }}" title="Megabyte Labs homepage" target="_blank">
      <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/home-solid.svg" />
    </a>
    <a href="{{ profile.dockerhub }}" title="Megabyte Labs profile on DockerHub" target="_blank">
      <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/dockerhub-profile-solid.svg" />
    </a>
    <a href="{{ website.dockerhub_repository }}/{{ slug }}" title="DockerHub page for this project" target="_blank">
      <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/dockerhub-image-solid.svg" />
    </a>
    <a href="{{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}/-/blob/master/CONTRIBUTING.md" title="Learn about contributing" target="_blank">
      <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/contribute-solid.svg" />
    </a>
    <a href="{{ profile.patreon }}" title="Support us on Patreon" target="_blank">
      <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/support-solid.svg" />
    </a>
    <a href="{{ chat_url }}" title="Slack chat room" target="_blank">
      <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/chat-solid.svg" />
    </a>
    <a href="{{ profile.github }}/docker-{{ slug_github }}" title="GitHub mirror" target="_blank">
      <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/github-solid.svg" />
    </a>
    <a href="{{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}" title="GitLab repository" target="_blank">
      <img src="https://gitlab.com/megabyte-labs/assets/-/raw/master/svg/gitlab-solid.svg" />
    </a>
  </h4>
  <p align="center">
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
    <img alt="GitHub: {{ profile.github }}" src="https://img.shields.io/github/followers/ProfessorManhattan?style=social" target="_blank" />
  </a>
  <a href="https://twitter.com/{{ profile.twitter }}" target="_blank">
    <img alt="Twitter: {{ profile.twitter }}" src="https://img.shields.io/twitter/url/https/twitter.com/{{ profile.twitter }}.svg?style=social&label=Follow%20%40{{ profile.twitter }}" />
  </a>
</p>
