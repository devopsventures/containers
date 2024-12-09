# Arguments that make up the base image tag so that we can inject these downstream
ARG DEVCONTAINER_NAME="javascript-node"
ARG DEVCONTAINER_VERSION="1.1.6"
ARG NODE_VERSION="22"
ARG OS_VARIANT="bookworm"

# The repository URL for the container builds
ARG image_url_base="https://github.com/peter-murray/development-containers"
# The container version
ARG version="unknown"
# The git commit SHA, needs injecting
ARG revision="unknown"
# Human readable description of the contents of the image
ARG description=""

# The tag for the container tag/verion that we are extending
ARG base_tag="${DEVCONTAINER_VERSION}-${NODE_VERSION}-${OS_VARIANT}"
# The full iamge for the container that we are extending, set as an argument only so we can reference it in labels later
ARG base_image="mcr.microsoft.com/devcontainers/${DEVCONTAINER_NAME}:${base_tag}"

FROM ${base_image}

# when switching containers, we need to redefine the arguments here so they can be referenced
ARG DEVCONTAINER_NAME
ARG DEVCONTAINER_VERSION
ARG OS_VARIANT
ARG image_url_base
ARG version
ARG revision
ARG description
ARG base_image
ARG base_tag

# Labels for the output container - common
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