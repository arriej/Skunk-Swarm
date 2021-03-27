# Traefikv2
What is traefik:
Traefik is a load balancer/proxy and does the following:
- Handles connections.
- Expose specific services and applications based on their domain names.
- Handle multiple domains (if you need to). Similar to "virtual hosts".
- Handle HTTPS.
- Acquire (generate) HTTPS certificates automatically (including renewals) with Let's Encrypt.
- Add HTTP Basic Auth for any service that you need to protect and doesn't have its own security, etc.
- Get all its configurations automatically from Docker labels set in your stacks (you don't need to update configuration files).

## how it works:
The idea is to have a main load balancer/proxy that covers all the Docker Swarm cluster and handles HTTPS certificates and requests for each domain.

But doing it in a way that allows you to have other Traefik services inside each stack without interfering with each other, to redirect based on path in the same stack (e.g. one container handles / for a web frontend and another handles /api for an API under the same domain), or to redirect from HTTP to HTTPS selectively.

## usage


## Current issues:
it's a copy from https://dockerswarm.rocks/traefik/#intro.
