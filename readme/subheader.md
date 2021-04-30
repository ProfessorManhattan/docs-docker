<h4>
  <a href="{{ website.homepage }}">Homepage</a>
  <span> | </span>
  <a href="{{ profile.dockerhub }}">DockerHub Profile</a>
  <span> | </span>
  <a href="{{ website.dockerhub_repository }}/{{ pkg.name }}">DockerHub Image</a>
  <span> | </span>
  <a href="{{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}/-/blob/master/CONTRIBUTING.md">Contributing</a>
  <span> | </span>
  <a href="{{ chat_url }}">Chat</a>
  <span> | </span>
  <a href="{{ profile.github }}/docker-{{ pkg.name }}">GitHub Mirror</a>
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
    <img alt="GitLab pipeline status" src="https://gitlab.com/megabyte-labs/dockerfile/{{ subgroup }}/{{ slug }}/badges/master/pipeline.svg" />
  </a>
  <a href="{{ repository.group.dockerfile }}/{{ subgroup }}/{{ slug }}/-/raw/master/LICENSE" target="_blank">
    <img alt="License: {{ license }}" src="https://img.shields.io/github/license/MegabyteLabs/docker-{{ slug }}?color=yellow&style={{ badge_style }}" />
  </a>
  <a href="https://github.com/{{ profile.github }}" target="_blank">
    <img alt="GitHub: {{ profile.github }}" src="https://img.shields.io/github/followers/MegabyteLabs?style=social" target="_blank" />
  </a>
  <a href="https://twitter.com/{{ profile.twitter }}" target="_blank">
    <img alt="Twitter: {{ profile.twitter }}" src="https://img.shields.io/twitter/follow/{{ profile.twitter }}.svg?style=social" />
  </a>
</p>
