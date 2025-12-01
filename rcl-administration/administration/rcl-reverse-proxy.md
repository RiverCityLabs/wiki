---
description: Reverse Proxy details
hidden: true
---

# RCL Reverse Proxy

We have implemented a reverse proxy server in order to securely serve local services over the internet.

## Install

In the unforunate event we need to reinstall the reverse proxy server, here are the steps to replicate it:

1. Install Raspberry Pi OS Lite (32bit) to a Sandisk Endurance Pro SD card (longer sd card life)
2. log in via ssh
3. run `sudo raspi-config`
   1. change the default pi password
   2. expand the filesystem
4. run `sudo apt update && apt upgrade`
5. run `curl -sSL https://get.docker.com | sh`
6. run `sudo usermod -aG docker pi`
7. run `sudo usermod -aG docker ${USER}` to set the permissions to the current user
8. run `sudo apt-get install -y libffi-dev libssl-dev`
9. run `sudo apt-get install -y python3 python3-pip`
10. run `sudo systemctl enable docker` to allow docker to start containers on boot
11. run `nano docker-compose.yml` and paste the following in:

```
version: '3'
services:
  app:
    image: 'jc21/nginx-proxy-manager:latest'
    restart: unless-stopped
    ports:
      - '80:80'
      - '81:81'
      - '443:443'
    volumes:
      - ./data:/data
      - ./letsencrypt:/etc/letsencrypt
```

12\. follow quick start instructions here: [https://nginxproxymanager.com/guide/#quick-setup](https://nginxproxymanager.com/guide/#quick-setup)\
13\. run `sudo nano etc/systemd/system/nginx-reverse-proxy-app.service`

paste the following in and save with `ctrl+x` -> `y` :

```
# /etc/systemd/system/nginx-reverse-proxy-app.service

[Unit]
Description=Docker Compose Application Service
Requires=docker.service
After=docker.service

[Service]
WorkingDirectory=/home/pi
ExecStart=/usr/local/bin/docker-compose up
ExecStop=/usr/local/bin/docker-compose down
TimeoutStartSec=0
Restart=on-failure
StartLimitIntervalSec=60
StartLimitBurst=3

[Install]
WantedBy=multi-user.target
```

14\. run `systemctl enable nginx-reverse-proxy-app.service` to enable it to run on boot
