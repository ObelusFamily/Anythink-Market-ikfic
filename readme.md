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

### Let's now run our application

Now, that docker is installed properly, we can run our app using following command in the root directory

```bash
$ sudo docker compose up
```

and then, enter the prompted admin password and all the images backend, db and frontend will start.

You can check on http://localhost:3000/api/ping, if the backend's working fine

and on http://localhost:3001/register, if the frontend's working fine.

If everything seems good, then create a user for yourself for local development.
