---
title: "Deploy Gitea and Woodpecker CI with Docker Compose"
date: 2022-11-13T15:05:00+02:00
author: Alexander
tags:
    - linux
    - docker
    - selfhosting
    - git
    - ci
categories:
    - "Tutorials"
---

Just a short post to let you know that I published my instructions on [Codeberg](https://codeberg.org) on how to quickly set up your own self-hosted Gitea server with Woodpecker CI and Traefik as a reverse proxy on your own local home server.

- [Docker Compose Traefik](https://codeberg.org/alexruf/docker-compose-traefik)
- [Docker Compose Gitea](https://codeberg.org/alexruf/docker-compose-gitea)
- [Docker Compose Woodpecker CI with Gitea integration](https://codeberg.org/alexruf/docker-compose-woodpecker-ci)

I have split everything up into individual Docker Compose files. You can also put everything together into on big Docker Compose if you like, but I prefer my components to be serperated nicely.

However, all the listed Docker Compose files somehow depend on each other, and therefore I recommend to set up all of them in order.

I hope this is helpful to anyone who wants to start self-hosting. If you have any questions, problems or suggestions for improvement, I would be happy if you contact me directly.
