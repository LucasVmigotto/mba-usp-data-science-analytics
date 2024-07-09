#syntax=docker/dockerfile:1
FROM mcr.microsoft.com/devcontainers/python:3.12

ARG USERNAME="vscode"
ARG POETRY_VERSION="1.8.3"

USER ${USERNAME}

RUN sudo apt-get update \
    && sudo apt-get upgrade -y

WORKDIR /app

RUN pipx install poetry=="${POETRY_VERSION}"

RUN pipx inject poetry poetry-plugin-export

COPY ./pyproject.toml ./poetry.lock* /app/

RUN poetry install --with dev

ENV PYTHONPATH=/app
