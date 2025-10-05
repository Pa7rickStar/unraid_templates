# Creating Unraid Docker containers from the comfort of my pineapple 🍍

## dawarich_db

This app sets up a [PostGIS](https://postgis.net) database container for Dawarich.

- Dawarich is a self-hosted web app designed to replace Google Timeline (aka Google Location History). Visualize your data on an interactive map, import your location history from Google Maps Timeline and Owntracks, and explore statistics like the number of countries and cities visited, total distance traveled, and more!
- PostGIS is a spatial database extender for PostgreSQL object-relational database. The postgis/postgis image provides tags for running Postgres with PostGIS extensions installed.

> [!NOTE]
>
> Do not use autoupdate and do not update any Dawarich container backing up your data first and checking for breaking changes in the updating guides.
>
> - [updating-guides](https://dawarich.app/docs/updating-guides)
> - [backup-and-restore](https://dawarich.app/docs/tutorials/backup-and-restore)

## dawarich_redis

This app sets up a [Redis](https://redis.io) database container for Dawarich.

- Dawarich is a self-hosted web app designed to replace Google Timeline (aka Google Location History). Visualize your data on an interactive map, import your location history from Google Maps Timeline and Owntracks, and explore statistics like the number of countries and cities visited, total distance traveled, and more!
- Redis is an open source (BSD licensed), in-memory data structure store, used as a database, cache and message broker. Based on official Redis Docker image.

> [!NOTE]
>
> Do not use autoupdate and do not update any Dawarich container backing up your data first and checking for breaking changes in the updating guides.
>
> - [updating-guides](https://dawarich.app/docs/updating-guides)
> - [backup-and-restore](https://dawarich.app/docs/tutorials/backup-and-restore)

## photon

[Photon](https://github.com/komoot/photon) is an open-source geocoding solution built for OpenStreetMap (OSM) data, providing features such as search-as-you-type and reverse geocoding.

This CA uses [rtuszik's unofficial Docker image](https://github.com/rtuszik/photon-docker/tree/main) for running Photon locally, enhancing data privacy and integration capabilities with services like Dawarich.

## Donate

I always try to make containers which work out of the box (for those who don't want to tinker around with docker) and use official sources as much as possible.

For my own repos you are welcome to <a href="https://www.buymeacoffee.com/pa7rickstar" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 25px !important;width: 90px !important;" ></a>
In case I'm just creating an unraid template for other peoples projects please consider donating to them instead.
