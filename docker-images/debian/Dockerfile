ARG BASE_IMAGE_NAME=debian
ARG BASE_IMAGE_TAG=8

FROM ${BASE_IMAGE_NAME}:${BASE_IMAGE_TAG}

LABEL mainteiner="Patricio Perpetua <patricio.perpetua.arg@gmail.com>" \
    name="singletonsd/docker/gitlab-ci-validator/debian" \
    architecture="x86_64" \
    vendor="SINGLETON" \
    vcs-type="git" \
    vcs-url="https://gitlab.com/singletonsd/docker/gitlab-ci-validator.git" \
    distribution-scope="private" \
    Summary="Image with gitlab-ci validator."

RUN apt-get update -qq && \
  apt-get install -qqy bash curl ca-certificates && \
  rm -rf /var/lib/apt/lists/*

COPY binaries/gitlab /usr/bin/

RUN chmod +x /usr/bin/gitlab
