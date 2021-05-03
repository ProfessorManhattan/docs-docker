## Requirements

Before getting started with development, you should ensure that the following requirements are present on your system:

* **[Docker]({{ repository.project.docker }})**

### Optional Requirements

* **[DockerSlim]({{ repository.project.dockerslim }})** - Used for generating compact, secure images
* **[jq]({{ repository.project.jq }}) - Used by `.start.sh` to interact with JSON documents from the bash shell
* **[Node.js]({{ repository.project.node }})** (*Version >=10*) - Utilized to add development features like a pre-commit hook and other automations

*Each of the requirements links to an Ansible Role that can install the dependency with a one-line bash script install.* Even if you do not have the optional dependencies installed, the `.start.sh` script (which is called by many of our build tool sequences) will attempt to install missing dependencies to the `~/.local/bin` folder.
