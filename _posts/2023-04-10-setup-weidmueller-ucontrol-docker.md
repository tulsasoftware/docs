---
layout: post
title: Setting Up Docker On Weidmueller U-Control UC20
subtitle: IIoT In Practice by Corey Thompson
cover-img: /assets/img/md/cowboy-code-sunrise1-1024x680.jpg
tags: [docker, weidmueller uc20, u-control uc20]
---

# How to set up weidmueller u-control docker

Weidmueller u-control docker is a feature that allows you to run your own or third-party software solutions on the u-control 2000 control system using container technology. This gives you more flexibility and portability for your industrial applications. The following steps will guide you through the installation and configuration of docker on u-control studio.

## Prerequisites

- You need a Weidmueller UC20-SL2000-OLAC (or similar) with “open linux”
- You need the engineering software u-create studio >= V1.20.2
- You need internet access on your PLC

## Steps

1. Connect your PLC to your PC using an Ethernet cable and open u-create studio.
2. In the project tree, right-click on your PLC and select "DevAdmin".
3. In the DevAdmin window, go to the "Network" tab and configure the IP address, subnet mask, gateway and DNS server for your PLC. Make sure that your PLC can access the internet.
4. Go to the "Software" tab and click on "Install Docker". This will download and install the docker package on your PLC.
5. After the installation is complete, click on "Start Docker". This will start the docker service on your PLC.
6. Go to the "Docker" tab and click on "Install Portainer". This will download and install the portainer package on your PLC.
7. After the installation is complete, click on "Start Portainer". This will start the portainer service on your PLC.
8. Go to the "Web" tab and click on "Open Portainer". This will open a web browser and direct you to the portainer web interface.
9. In the portainer web interface, create a user account and log in.
10. In the portainer dashboard, click on "Local" under "Endpoints". This will connect you to the local docker engine on your PLC.
11. In the portainer menu, click on "Containers". This will show you a list of existing containers on your PLC.
12. To create a new container, click on "Add container". This will open a form where you can specify the name, image, ports, volumes, environment variables and other settings for your container.
13. To find an image for your container, you can use the search bar at the top of the form or browse through the available images in the portainer registry.
14. After filling in the required fields, click on "Deploy the container". This will pull the image from the registry and create a new container on your PLC.
15. To start, stop, restart or remove a container, you can use the buttons at the right side of each container in the list.
16. To view or edit the details of a container, you can click on its name in the list.

## Next Steps

Now you're setup and ready to run a Docker app of your choosing. For inspiration on your next steps, read our upcoming article over running Node-RED in Docker on your UC20.

Happy coding!

## References

1. [UC20-SL2000-OLAC-EC Quick Start Guide for docker on u-control studio](https://mdcop.weidmueller.com/awp/A/Weidmueller_Assets/225511)