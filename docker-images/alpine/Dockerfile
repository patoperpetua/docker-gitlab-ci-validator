ARG BASE_IMAGE_NAME=alpine
ARG BASE_IMAGE_TAG=3.7

FROM ${BASE_IMAGE_NAME}:${BASE_IMAGE_TAG}

LABEL mainteiner="Patricio Perpetua <patricio.perpetua.arg@gmail.com>" \
    name="singletonsd/docker/gitlab-ci-validator/alpine" \
    architecture="x86_64" \
    vendor="SINGLETON" \
    vcs-type="git" \
    vcs-url="https://gitlab.com/singletonsd/docker/gitlab-ci-validator.git" \
    distribution-scope="private" \
    Summary="Image with gitlab-ci validator."

RUN apk add --no-cache bash curl ca-certificates && \
  rm -rf /var/lib/apt/lists/*

COPY binaries/gitlab /usr/bin/

RUN chmod +x /usr/bin/gitlab
