FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye

USER vscode

RUN <<eof
    sudo apt update
    sudo apt install --yes libxkbcommon-dev libgl-dev libegl1 libdbus-1-3
    sudo rm -fr /var/lib/apt/lists/*
eof

WORKDIR /workspaces/qt-project

COPY requirements.txt .

RUN <<eof
    python -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
eof
