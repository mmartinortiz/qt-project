FROM mcr.microsoft.com/devcontainers/python:1-3.12-bookworm

USER vscode

RUN <<eof
    sudo apt update
    sudo apt install --yes libxkbcommon-dev libgl-dev libegl1 libdbus-1-3 qt6-wayland
    sudo rm -fr /var/lib/apt/lists/*
eof
