<h4>
  <a href="">DockerHub Profile</a>
  <span> | </span>
  <a href="">DockerHub Image</a>
  <span> | </span>
  <a href="{{ repository.group.dockerfile }}/{{ SUBGROUP }}/{{ SLUG }}/-/blob/master/CONTRIBUTING.md">Contributing</a>
  <span> | </span>
  <a href="{{ chat_url }}">Chat</a>
  <span> | </span>
  <a href="{{ website.homepage }}">Website</a>
</h4>
<p>
  <a href="{{ repository.group.dockerfile }}/{{ SUBGROUP }}/{{ SLUG }}">
    <img alt="Version" src="https://img.shields.io/badge/version-{{ version }}-blue.svg?cacheSeconds=2592000" />
  </a>
  <a href="{{ website.documentation }}/docker" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="{{ repository.group.dockerfile }}/{{ SUBGROUP }}/{{ SLUG }}/-/raw/master/LICENSE" target="_blank">
    <img alt="License: {{ license }}" src="https://img.shields.io/badge/License-{{ license }}-yellow.svg" />
  </a>
  <a href="https://twitter.com/{{ profile.twitter }}" target="_blank">
    <img alt="Twitter: {{ profile.twitter }}" src="https://img.shields.io/twitter/follow/{{ profile.twitter }}.svg?style=social" />
  </a>
</p>
