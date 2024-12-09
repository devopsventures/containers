ARG CONTAINER_NAME="ubuntu"
ARG VARIANT="24.04"

ARG image_url_base="https://github.com/peter-murray/development-containers"

# The git commit SHA
ARG revision=""
# Human readable description of the contents of the image
ARG description=""
# The base image that we are extending
ARG base_image="docker.io/${CONTAINER_NAME}:${VARIANT}"

FROM ${base_image}

# when extending the container definitions need to redefine the arguments here so they can be referenced
ARG VARIANT

ARG image_url_base
ARG revision
ARG desctiption
ARG base_image

LABEL org.opencontainers.image.authors="peter-murray" \
  org.opencontainers.image.base.name="${base_image}" \
  org.opencontainers.image.url="${image_url_base}" \
  org.opencontainers.image.documentation="${image_url_base}/README.md" \
  org.opencontainers.image.source="${image_url_base}" \
  org.opencontainers.image.version="${version}" \
  org.opencontainers.image.revision="${revision}" \
  org.opencontainers.image.vendor="peter-murray" \
  org.opencontainers.image.licenses="MIT" \
  org.opencontainers.image.title="peter-murray/development-containers - ${CONTAINER_NAME}-${VARIANT}" \
  org.opencontainers.image.description="${description}"