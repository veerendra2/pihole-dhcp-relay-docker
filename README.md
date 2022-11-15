# Pihole with DHCP relay in Docker
Run Pi-hole in bridge mode with DHCP relay.
> Created this repo for my blog: [https://veerendra2.github.io/pihole-dhcp-relay/](https://veerendra2.github.io/pihole-dhcp-relay/)

* Pi-hole [docs](https://docs.pi-hole.net/docker/DHCP/)
## Configure
* DHCP
  * Enable and DHCP pool in [.env#L14](./.env#L14)
  * DHCP options to set Pi-hole DNS IP in [dnsmasq.d/07-dhcp-options.conf](./dnsmasq.d/07-dhcp-options.conf)
* DNS
  * Add custom DNS records in [pihole/custom.list](./pihole/custom.list)
* More environmental variables https://github.com/pi-hole/docker-pi-hole/#optional-variables
## Deploy
```
$ git clone https://github.com/veerendra2/pihole-dhcp-relay-docker.git
$ cd pihole-dhcp-relay-docker

# Configure Pi-hole
$ docker-compose up -d
```