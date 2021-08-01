# PiHole with cloudflared (DoH)

## About

This is a PiHole image that uses DNS over HTTPS client **cloudflared** to safely query the upstream Cloudflare DNS. DNS
over HTTPS ensures safe communication between DNS resolvers and prevents malicious injections.

Check out the [article.](https://medium.com/codex/pi-hole-and-doh-f1a9f8acd0f7)

## Deploying PiHole

### Docker

1. Build the image:

   > docker build -t pihole .

2. Run the container:

   > docker run -d -p "53:53" -p  "67:67/udp" -p "53:53/udp" -e "WEBPASSWORD=yourwebpass" pihole

### Docker-compose

Simply run:

> docker-compose up -d 