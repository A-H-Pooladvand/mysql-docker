# Laravel | Lumen Docker

The php [Laravel | Lumen] docker project

## Getting started
- [Install requirements](#install-requirements)
- [Quick start](#quick-start)

### Install requirements
**Git**

```shell
# Debian
sudo apt install git
```
**Make**

```shell
# Debian
sudo apt install make
```
**Docker & Docker Compose**

```shell
# Install docker & compose
# docker-compose included when installing via convenient script
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
# To run Docker without root privileges
sudo groupadd docker # Create the docker group. 
sudo usermod -aG docker $USER #Add your user to the docker group.
sudo newgrp docker # Activate 
```

### Quick Start
- Check the `.env` file and set environment variables
- Check `Makefile` and set `PROJECT_NAME`
  - The `PROJECT_NAME` in `Makefile` must be identical with the `PROJECT_NAME` in the `.env` file
- `clone` your krakend project into `./src/` directory
- To install and start the container run `make build && make watch`

**To list all available commands please run**  

```shell
make help
```