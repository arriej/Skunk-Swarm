# Skunk-Swarm
the Skunk swarm repo is meant to be informational and used as a reference for my self and others when creating a docker-swarm on raspberry pi's.
Along with traefik v2 managing the internet exposed containers.  

I run all these containers on my 3 raspberry pi 4's ((manager)1x4GB (workers)2x8GB) All 3 pi's have a 128GB SSD card.

# Concept design
The concept of the swarm is that there is 1 general storage location over 3 or 4 raspberry pi's, all services that are internet exposed will run trough traefikv2.
So all compose files will have flags for traefikv2 instead v1.
The swarm exist out of:


# Configs in this repo:
Please note these configs are currently not functional without setting up paths before starting the stacks.
This is a work in progress to Standardize the configs, and use uniform paths to 1 storage location

Container | Description | Additional
----------|----------|----------
Traefikv2 | Traefik reverse proxy | [Hub](https://hub.docker.com/_/traefik) - [Docs](https://docs.traefik.io/)
Portainer | Docker Management GUI | [Hub](https://hub.docker.com/r/portainer/portainer)
bookstack | organizing and storing information (Alternative for wiki.js) | [Hub](https://hub.docker.com/r/linuxserver/bookstack) - [Website](https://www.bookstackapp.com/)
Wiki.js | wiki building (alternative for bookstack) | [Hub](https://hub.docker.com/r/requarks/wiki) - [Website](https://js.wiki/)

## What I want to add:

Container | Description | Additional
----------|----------|----------
BitWarden_rs | Password manager | [Hub](https://hub.docker.com/r/bitwardenrs/server)
Firefly | Money manager | [Hub](https://hub.docker.com/r/jc5x/firefly-iii)
Guacamole | Client-less remote desktop gateway | [Hub](https://hub.docker.com/r/oznu/guacamole/)
Netdata | Performance monitoring | [Hub](https://hub.docker.com/r/netdata/netdata/)
Nextcloud | A safe home for all your data | [Hub](https://hub.docker.com/_/nextcloud)
Pi-hole | Network based ad blocker | [Hub](https://hub.docker.com/r/pihole/pihole) - [Website](https://pi-hole.net/)
Watchtower | Container auto-updates | [Hub](https://hub.docker.com/r/v2tec/watchtower)
Rainloop | Webmail client | [Hub](https://hub.docker.com/r/hardware/rainloop/) - [Website](https://www.rainloop.net/)
Mailcow | Mail server suite | [GitHub](https://github.com/mailcow/mailcow-dockerized) - [Website](https://mailcow.email/)
Paperless ng | Change paper into digital documents | [GitHub](https://github.com/jonaswinkler/paperless-ng) - [Website](https://paperless-ng.readthedocs.io/en/latest/setup.html#setup-docker-hub)
SSGWify | Web SSHclient | [Hub](https://hub.docker.com/r/niruix/sshwifty)
heimdall | Dashboard (maybe different one?) | [Hub](https://hub.docker.com/r/linuxserver/heimdall/) - [Website](https://heimdall.site/)
N8n | Self host IFTTT | [Hub](https://hub.docker.com/r/n8nio/n8n) - [Website](https://n8n.io/)


### Todo:
[]Standardize configs.
[]Remove unassay information from configs
[]Reduce workers SD cards to small ones. with 1 storage location on NAS. (and use this one location in all configs)

##### Contributing

Feel free to fork and submit pull requests to this repo
