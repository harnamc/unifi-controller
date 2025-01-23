# Unifi Controller

The way Ubiquiti resources are configures are through a Unifi Controller. This repo setups use a Unifi Controller using the `lscr.io/linuxserver/unifi-network-application` image and official `docker.io/mongo` image. The image tags are controlled in the `.env`.

## Setup

* Follow the instructions outlined here for Docker install: https://docs.docker.com/engine/install/
* Create a `.env` using: `cp .env.example .env`.
* Add values to the `.env` file.
* Create folder on the host that will map to the containers volume: `mkdir -p /config /mongo/db /mongo/configdb`

## Usage

* Create the containers using: `docker-compose up -d`
* Expose the following host ports needed send traffic from host to containers: `8443, 3478/udp, 10001/udp, 8080`
