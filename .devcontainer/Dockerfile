FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

# Copies mise binary from mise docker image on dockerhub
COPY --from=jdxcode/mise /usr/local/bin/mise /usr/local/bin/

RUN apt-get update && apt-get install -y vim kubectx

# make sure mise is activated in both zsh and bash. Might be overridden by a user's dotfiles.
RUN echo 'eval "$(mise activate bash)"' >> /home/vscode/.bashrc && \
    echo 'eval "$(mise activate zsh)"' >> /home/vscode/.zshrc
