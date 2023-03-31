---
layout: post
title: WHAT DOES A "DOCKER-COMPOSE" FILE DO?
subtitle: Leveraging IIoT In Practice by Corey Thompson
cover-img: /assets/img/docker-compose-stack.png
tags: [docker, compose]
---

So you've found a file on your file system maybe after a clone of a repository, "docker-compose.yml", and don't know what it is or what to do with it. Should you keep it, delete it or edit it? Depends on what your intention of the code you're using are, it's possibly a very helpful file!

In brief - it's a configuration file used to orchestrate the launch of multiple dependent Docker containers. If you've done development with Docker, you've likely used the CLI command `docker run` to launch individual containerized applications and used lots of parameters like "-v" or "-p" to map all of its input and output communications. This file exists to prevent the need to individually call `docker run ...` on each application and document all of those commands for an entire system, allowing you to version control the setup if desired. This file is launched using a separate binary called `docker-compose` and while in the directory of your `docker-compose.yml` with your Docker daemon running, you simply need to run the CLI command `docker-compose up" and it will launch all of the defined containers on the current local host using the configured settings.

To learn more, be sure to study the docs to learn about support versions of the Docker engine, as some older versions of Docker require you to install `docker-compose` separately while newer versions bundle it in.