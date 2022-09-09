# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## First setup

This Setup is for Linux (Ubuntu 22.04LTS and higher)

### Let's remove already installed docker first:

```bash
$ sudo apt remove docker-desktop
```

Do this, for a complete removal:

```bash
$ rm -r $HOME/.docker/desktop
$ sudo rm /usr/local/bin/com.docker.cli
$ sudo apt purge docker-desktop
```

### Let's install Docker

Set up [Docker’s package repository](https://docs.docker.com/engine/install/ubuntu/#set-up-the-repository).

Download [latest DEB package](https://desktop.docker.com/linux/main/amd64/docker-desktop-4.11.0-amd64.deb?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-linux-amd64).

Install the package with apt as follows:

```bash
$ sudo apt-get update
$ sudo apt-get install ./docker-desktop-<version>-<arch>.deb
```

### Launch Docker Desktop

```bash
$ systemctl --user start docker-desktop
```

and check, if you've successfully installed Docker Desktop:

```bash
$ docker compose version
```
