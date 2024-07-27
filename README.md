# usp-mba-data-science-analytics

[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-%23FE5196?logo=conventionalcommits&logoColor=white)](https://conventionalcommits.org)

Atividades do curso de MBA da USP em Data Science and Analytics

## Getting started

Clone the repository into the desire folder

* With `ssh`

    ```bash
    git clone git@github.com:LucasVmigotto/.datascience-slim.git
    ```

* With `HTTPS`

    ```bash
    git clone https://github.com/LucasVmigotto/.datascience-slim.git
    ```

* With GitHub CLI

    ```bash
    gh repo clone LucasVmigotto/.datascience-slim
    ```

## Pre requisites

### Mandatory

* [Docker Engine](https://docs.docker.com/engine/)
* [Visual Studio Code](https://code.visualstudio.com/)
* [VSCode Extension Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Using Docker

### Dev container environment

This is a basic environment prepared to start some application development. It comes with [Python](https://www.python.org/), [`git`](https://git-scm.com/) and [`zsh`](https://www.zsh.org/) with [Oh My Zsh](https://ohmyz.sh/)!

The [IPykernel](https://ipython.readthedocs.io/en/stable/index.html) package is also installed to manage kernel use with Jupyter Notebooks.

### Docker Troubleshooting

List all Docker containers

```bash
docker ps -a
```

Remove Docker Compose containers

```bash
docker compose rm --stop -f
```

Prune containers

```bash
docker container prune --force
```

List all Docker images

```bash
docker ls -a
```

Remove Docker _dangling_ images

```bash
docker image rm -f $(docker image ls --filter "dangling=true" -aq)
```

List all Docker volumes

```bash
docker volume ls
```

Prune Docker volumes

```bash
docker volume prune --force
```

> **WARNING**: If you want to remove **ALL** Docker images, just remove the `--filter` flag and argument
>
> `docker image rm -f $(docker image ls -aq)`

## References

* [Visual Studio Code Dev Container creation](https://code.visualstudio.com/docs/devcontainers/create-dev-container)
* [Dev Container](https://containers.dev/)
* [Dev Container images](https://github.com/devcontainers/images/tree/main/src)
* [Docker](https://docs.docker.com/)
* [Fast.ai Course 22 repository](https://github.com/fastai/course22)
