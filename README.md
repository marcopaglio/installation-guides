
# Docker

ABOUT

## Docker Engine

TODO

### Installation Guide

The installation guide depending on your operating system.

#### Linux

A complete step-by-step guide is provided by the [Docker official webpage](https://docs.docker.com/engine/install/ubuntu/). It follows an essential extract:

1. Before you can install Docker Engine, you need to uninstall any conflicting packages by running the following command:
   ```
   for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
   ```
   `apt-get` might report that you have none of these packages installed.
   
2. Before you install Docker Engine *for the first time* on a new host machine, you need to set up the Docker repository by running following commands:
   ```
   # Add Docker's official GPG key:
   sudo apt-get update
   sudo apt-get install ca-certificates curl gnupg
   sudo install -m 0755 -d /etc/apt/keyrings
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
   sudo chmod a+r /etc/apt/keyrings/docker.gpg

   # Add the repository to Apt sources:
   echo \
     "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
     $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
     sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   sudo apt-get update
   ```
   
3. To install the latest version of Docker Engine (and also Docker Compose), run:
   ```
   sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
   ```
   
4. Verify that the Docker Engine installation is successful by running the `hello-world` image:
   ```
   sudo docker run hello-world
   ```
   This command downloads a test image and runs it in a container. When the container runs, it prints a confirmation message and exits.

In Linux, Docker commands must be run as the superuser. Add your user to the docker group by running the following command:
```
sudo usermod -aG docker ${USER}
```
After that, you need to logout and login again. Then, you can run Docker commands without using `sudo` with your user.

## Docker Compose

TODO

### Installation Guide

The installation guide depending on your operating system.

#### Linux (Ubuntu)

Follow the [Docker Engine Installation Guide](#installation-guide) to install Docker Compose, too.
