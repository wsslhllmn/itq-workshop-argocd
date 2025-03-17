FROM mcr.microsoft.com/devcontainers/python

COPY --from=ghcr.io/charmbracelet/gum:v0.14.1 /usr/local/bin/gum /usr/local/bin/gum

RUN sudo apt update && sudo apt install -y --no-install-recommends \
  entr git

RUN git clone https://github.com/ahmetb/kubectx /opt/kubectx
RUN ln -s /opt/kubectx/kubectx /usr/local/bin/kubectx
RUN ln -s /opt/kubectx/kubens /usr/local/bin/kubens
