---
layout: post
title: How to Use Node-RED With Weidmueller U-Control UC20
subtitle: IIoT In Practice by Corey Thompson
cover-img: /assets/img/md/cowboy-code-sunrise2-1024x680.jpg
tags: [docker, weidmueller uc20, u-control uc20, node-red]
---

# How to use Node-RED with u-control docker

Node-RED is a flow-based programming tool for wiring together hardware devices, APIs and online services. It can be used to create IoT applications and integrate different systems. Node-RED is already integrated into the u-control 2000 control system as a software module, but you can also run it as a docker container on u-control docker. This gives you more flexibility and control over the Node-RED version and configuration. The following steps will guide you through the process of running Node-RED as a docker container on u-control docker.

## Prerequisites

- You need a Weidmueller UC20-SL2000-OLAC (or similar) with “open linux”
- You need the engineering software u-create studio >= V1.20.2
- You need internet access on your PLC
- You need docker and portainer installed and running on your PLC. [Read our post on setting it up](({% post_url /2023-04-10-setup-weidmueller-ucontrol-docker %}))

## Steps

1. Connect your PLC to your PC using an Ethernet cable and open u-create studio.
2. In the project tree, right-click on your PLC and select "DevAdmin".
3. In the DevAdmin window, go to the "Web" tab and click on "Open Portainer". This will open a web browser and direct you to the portainer web interface.
4. In the portainer web interface, log in with your user account.
5. In the portainer dashboard, click on "Local" under "Endpoints". This will connect you to the local docker engine on your PLC.
6. In the portainer menu, click on "Containers". This will show you a list of existing containers on your PLC.
7. To create a new container for Node-RED, click on "Add container". This will open a form where you can specify the name, image, ports, volumes, environment variables and other settings for your container.
8. In the form, enter the following values:

    - Name: node-red (or any name you like)
    - Image: nodered/node-red (this is the official Node-RED image from Docker Hub)
    - Port mapping: add a port mapping from host port 1880 to container port 1880 (this will allow you to access the Node-RED editor from your browser)
    - Volume mapping: add a volume mapping from host directory node_red_data to container directory /data (this will persist your Node-RED flows and settings)
    - Restart policy: always (this will ensure that your container restarts automatically if it stops or crashes)

9. After filling in the required fields, click on "Deploy the container". This will pull the image from Docker Hub and create a new container on your PLC.
10. To start, stop, restart or remove your container, you can use the buttons at the right side of each container in the list.
11. To view or edit the details of your container, you can click on its name in the list.
12. To access the Node-RED editor, open a web browser and go to http:// {host-ip}:1880 (replace {host-ip} with the IP address of your PLC). You should see the familiar Node-RED desktop where you can create and deploy your flows.

## References

1. [Running under Docker : Node-RED](https://nodered.org/docs/getting-started/docker)
2. [node-red/node-red-docker - Github](https://github.com/node-red/node-red-docker)
3. [Node-RED Docker+Kubernetes — Technically Wizardry](https://www.technicallywizardry.com/node-red-docker-kubernetes/)
4. [node-red-contrib-dockerode (node) - Node-RED](https://flows.nodered.org/node/node-red-contrib-dockerode)