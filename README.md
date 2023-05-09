# Anaconda and Miniconda Docker Images and Documentation

Docker images for Anaconda/Miniconda that are available from DockerHub:

https://hub.docker.com/r/continuumio/

Documentation for Anaconda Integrations, including Docker:
Anaconda 集成文档，包括 Docker

https://docs.anaconda.com/anaconda/user-guide/tasks/docker/

Package build images hosted on ECR can be found here:

https://gallery.ecr.aws/y0o4y9o3/anaconda-pkg-build

Package build images hosted on DockerHub can be found here:

https://hub.docker.com/r/continuumio/anaconda-pkg-build/tags?page=1&ordering=last_updated


| image                          | description                                                  | version |
| ------------------------------ | ------------------------------------------------------------ | ------- |
| continuumio/anaconda3          | Container with a bootstrapped Anaconda installation          | ![](https://img.shields.io/docker/v/continuumio/anaconda3?sort=semver)          |
| continuumio/miniconda3         | Container with a bootstrapped Miniconda installation         | ![](https://img.shields.io/docker/v/continuumio/miniconda3?sort=semver)         |
| continuumio/anaconda-pkg-build | Container with a bootstrapped Anaconda installation with GCC | ![](https://img.shields.io/docker/v/continuumio/anaconda-pkg-build?sort=semver) |
