# Creating Unraid Docker containers from the comfort of my pineapple 🍍

## dawarich_app

[Dawarich](https://dawarich.app) is a self-hosted alternative to Google Timeline (Google Location History). Visualize location history on an interactive map, import location data and explore travel statistics.

The production setup requires three containers on the `dawarich` Docker network:

- `dawarich_app` — Web application with embedded Sidekiq for background jobs
- `dawarich_db` — PostgreSQL database with PostGIS
- `dawarich_redis` — Redis for caching and background jobs

### Documentation

- [Unraid installation](https://dawarich.app/docs/self-hosting/installation/unraid/)
- [Environment variables](https://dawarich.app/docs/self-hosting/environment-variables/)
- [Updating guides](https://dawarich.app/docs/self-hosting/updating/)
- [Backup and restore](https://dawarich.app/docs/self-hosting/maintenance/backup-and-restore/)

> [!IMPORTANT]
> Do not enable automatic updates for Dawarich containers. Back up the database and persistent files, review the updating guides for breaking changes, and complete any required migrations before updating further.

## dawarich_db

A [PostGIS](https://postgis.net) database container for Dawarich, based on the [postgis/postgis](https://hub.docker.com/r/postgis/postgis) Docker image.

Uses PostgreSQL 17 with PostGIS 3.5 and persistent database storage.

## dawarich_redis

A [Redis](https://redis.io) container for Dawarich, based on the [official Redis Docker image](https://hub.docker.com/_/redis).

Provides caching and background-job queues, with persistent storage for Redis data.

## photon

[Photon](https://github.com/komoot/photon) is an open-source geocoding solution based on OpenStreetMap (OSM), supporting address search, search-as-you-type, and reverse geocoding.

This template uses [rtuszik's unofficial Photon Docker image](https://github.com/rtuszik/photon-docker) to run Photon locally, offering a self-hosted geocoding service for applications such as Dawarich.

## Donate

I aim to create unRAID templates that work out of the box, using official sources wherever possible.

For my own projects, you're welcome to <a href="https://www.buymeacoffee.com/pa7rickstar" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 25px !important;width: 90px !important;" ></a>
When I'm just providing an unRAID template for someone else's project, please consider donating to the original developers instead.
