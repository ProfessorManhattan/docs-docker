## Overview

All our Dockerfiles are created for specific tasks. In many cases, this allows us to reduce the size of the Dockerfiles by removing unnecessary files and performing other optimizations. Our Dockerfiles are broken down into the following categories:

* [**Ansible Molecule**]() - Dockerfile projects used to generate pre-built Docker containers that are intended for use by Ansible Molecule
* [**Apps**]() - Full-fledged web applications
* [**CI Pipeline**]()** - Projects that include tools used during deployments such as linters and auto-formatters
* [**Software**]() - Docker containers that are meant to replace software that is traditionally installed directly on hosts
