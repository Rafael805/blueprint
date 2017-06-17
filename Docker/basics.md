# Getting Started

You can easily get started with Docker if you install the Docker Toolbox: it contains all the tools you need to get your containers up and running. Follow the installation instructions, select the "Docker QuickStart Terminal" and indicate to install the Kitematic Visual Management tool too if you don't have it or any other virtualization platform installed.

The installation through the Docker Quickstart Terminal can take some time but then you're good to go. Use the command docker run to run Docker "images". You can consider these images as pre-packaged bundles of software that can be automatically downloaded from the Docker Hub when you run them.

Tip: browse the Docker Image Library for thousands of the most popular software tools. You will find also other notebooks that you can run in your Docker container, such as the Data Science Notebook, the R Notebook, and many more.


# Fundamentals 
The key thing to know about Docker is that **any changes you make inside the container will be lost when you exit**. If you want to save any changes, you need to explicitly commit them.

## Docker essentials

Here are some basics:
+ Run ```docker --help``` to see commands, or use that option to find out more about a specific command, e.g. ```docker image --help```. To list your Docker images, run ```docker image ls```.
+ Use docker ```run -it <image_tag>``` to start a new instance of a container from the tagged image.
+ Once in a container, type ```exit``` to stop and leave your virtual machine. Any uncommitted changes will be lost!
+ Use docker ```images``` or ```docker ps``` to see what Docker images or processes are running.

# Images

An image is a lightweight, stand-alone, executable package that includes everything needed to run a piece of software, including the code, a runtime, libraries, environment variables, and config files. It is a read-only template with instructions for creating a Docker container. Often, an image is based on another image, with some additional customization.

# Containers

A container is a runtime instance of a docker image.

A Docker container consists of

+ A Docker image
+ An execution environment
+ A standard set of instructions

Docker is an excellent platform to run software in containers. These containers are self-contained and isolated processes. A container is a runnable instance of an image. By default, a container is relatively well isolated from other containers and its host machine. You can control how isolated a container’s network, storage, or other underlying subsystems are from other containers or from the host machine.

You can kill a container and free up the port by using: 
```
docker kill <container_id>
```

# Saving changes to a Docket container 
After running our Docker image (in another window), we can run
```
docker ps
```

--example output: 
```
CONTAINER ID  IMAGE              COMMAND     CREATED                                  
**68f8994d3b19**  <image>:<version>  "/bin/bash" 7 hours ago
STATUS      PORTS               NAMES
Up 7 hours  6006/tcp, 8888/tcp  epic_minsky
```

After we’ve made some changes in the container, we use the CONTAINER ID to commit the changes:

```docker commit 68f8994d3b19 danjarvis/tensorflow-android:1.0.0```

# Publishing a Docker container
Go to https://hub.docker.com and create yourself an account. Use ```docker login``` and ```docker push``` to push your tagged Docker image to your Docker account.
