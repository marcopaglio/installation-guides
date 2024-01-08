
# Docker

ABOUT

## Installation Guide

The installation guide depending on your operating system.

### Windows

A complete step-by-step guide is provided by the [Docker official webpage](https://docs.docker.com/desktop/install/windows-install/). It follows an essential extract:

1. Install the last version of WSL from the [Microsoft Store](https://aka.ms/wslstorepage) or update it if a previous version is already installed through `wsl --update`.

2. Download the Docker Desktop installer.

3. Follow the wizard instructions to authorize the installer and proceed with the installation.

#### Setup for Maven

If your aim is using Docker with Maven through [docker-maven-plugin](https://github.com/fabric8io/docker-maven-plugin), some stardard configuration must be changed.<br>

By default, on Windows the Docker daemon is accessible through a named pipe instead of a socket (as in Linux and macOS). When the docker-maven-plugin goals are executed such pipe instances quickly become busy making the goals fail with the following error:
```
Error: DOCKER> Cannot create docker access object [\\.\pipe\docker_engine (All pipe instances are busy)]
```
In order to solve the problem: access the **General Settings** dialog of Docker Desktop > enable `Expose daemon on tcp://localhost:2375…` > **Apply and restart** > close Docker (**Quit Docker Desktop**) and restart it for the changes to be applied.<br>

Then, we have to tell the Docker client and the docker-maven-plugin that the Docker daemon is listening on that TCP address. This can be done by setting the standard Docker environment variable `DOCKER_HOST` (which is read by docker-maven-plugin as well). Run the following command on a Command Prompt as Administrator:
```
setx DOCKER_HOST tcp://localhost:2375 -m
```

### Linux

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

On Linux, Docker commands must be run as the superuser. Add your user to the docker group by running the following command:
```
sudo usermod -aG docker ${USER}
```
After that, you need to logout and login again. Then, you can run Docker commands without using `sudo` with your user.
