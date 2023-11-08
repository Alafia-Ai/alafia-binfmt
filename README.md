# alafia-binfmt

## Description

Alafia-specific deployment of [binfmt](https://github.com/tonistiigi/binfmt) based on [the official Docker image](https://registry.hub.docker.com/r/tonistiigi/binfmt). This app is mostly hidden from the user. It contains essentially just a systemd service file that is required for other applications. binfmt provides qemu-user shims to run amd64 / x86_64 docker containers.

## Usage

Meant to be used as a submodule in [alafia-apps](https://github.com/Alafia-Ai/alafia-apps).

`Makefile` can be manually invoked with the following options:

- `make` or `make build`: Locally build the Docker image
- `make install`: Install the files in the `deploy/` directory, and if relevant, install systemd service files and modify `/etc/hosts/`
- `make uninstall`: Removes all installed files, and if relevant, removes systemd services and resets `/etc/hosts/` 
