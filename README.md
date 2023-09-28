# run_ntfy

This is a simple repository for running ntfy and cloudflare tunnel on a home server.

It appears that running the docker containers on separate docker networks does not resolve properly when off the some network as the home server. 

This configuration works with iOS, home server, and cloudflare.  Tested on home WiFI and 5G service.

This repository is a result of [issue #888](https://github.com/binwiederhier/ntfy/issues/888) within the ntfy repository.

## Settings

Adjust the server.yml base-url as appropriate for your server domain.

## Configure Cloudflare

Configure your cloudflare tunnel as follows:

- subdomain: ntfy
- domain: mydomain.com
- path: (empty)
- type: HTTP
- url: ntfy

## Configure Docker-Compose File

1. Set your timezone as appropriate
2. Set you volumes location, use the current location or set another by moving your settings.yml file to new location
3. In tunnel command change 'mysecretkey' with your private key from cloudflare

