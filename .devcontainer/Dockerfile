# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.245.2/containers/debian/.devcontainer/base.Dockerfile

# [Choice] Debian version (use bullseye on local arm64/Apple Silicon): bullseye, buster
ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# ** [Optional] Uncomment this section to install additional packages. **
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive
    # && apt-get -y install --no-install-recommends <your-package-list-here>
RUN apt-get install -y gnupg
RUN echo 'deb http://download.opensuse.org/repositories/devel:/languages:/crystal/Debian_Unstable/ /' | sudo tee /etc/apt/sources.list.d/devel:languages:crystal.list
RUN curl -fsSL https://download.opensuse.org/repositories/devel:languages:crystal/Debian_Unstable/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/devel_languages_crystal.gpg > /dev/null
RUN sudo apt update
RUN sudo apt install -y crystal

