# Minecraft Remote RCON Interface (minecraft-remote-rcon-interface)

A front-end for consuming the remote-minecraft-rcon-cli API

## Project Links

- Localhost: [http://localhost:9000](http://localhost:9000)
- Staging: TBD
- Production: TBD

## Getting Started

To run this code you'll need to

- use a UNIX operating system
- have [Docker](https://www.docker.com/) installed

### Quick Start

Locally, using docker is the easiest and fastest way to get up and running. The `docker-compose.yaml` file will start the following services for you:

- Node, running quasar dev mapped to your host by default to port 9000

1. Clone the repository and change directory into the cloned repo

```bash
git clone git@github.com:noahjahn/minecraft-remote-rcon-interface.git
cd minecraft-remote-rcon-interface
```

2. Set up the `.env` file

```
cp .env.example .env
```

3. Start docker containers (this will take a while the first time, grab a cup of coffee)

```bash
./start
```

- You can optionally pass a port number to map nodejs to your host on a different port than the default of 8080. Ex: `./start 80`
- The start command leaves the container logs attached to your terminal so you can troubleshoot and view errors and warnings
  - If you lose the container logs, you can get them back by running `docker compose logs -f ` from the root of the project

### Stopping the application

Using the `./start` script keeps the application container logs attached to your terminal. Pressing Ctrl + C on that terminal will stop and remove the containers.

If you don't have the container logs attached to your terminal anymore you can run `docker compose down` from the root of the project to stop and remove the containers.

## Additional notes from Quasar

### Lint the files

```bash
./npm run lint
```

### Format the files

```bash
./npm run format
```

### Build the app for production

```bash
./npm run build
```

### Customize the configuration

See [Configuring quasar.config.js](https://v2.quasar.dev/quasar-cli-vite/quasar-config-js).
