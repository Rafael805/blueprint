# Introduction to Docker & Docker Containers

# What is Docker?

If you’ve been following trends in the “cloud” world, you’ve probably heard of Docker. The best way to describe Docker is to use the phrase from the Docker web site—Docker is

“an open source project to pack, ship and run any application as a lightweight container.” 

Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications.

# How is it Useful?

--example:

What if you have 3 application each using Ruby on Rails. What if each application needed a different version of Ruby on Rails but the Ruby on Rails version we have on our computer is version 3. The application that needs version 3 is working fine but the other two fail.

How do we fix this?

Solution 1: Have a different computer for each application.

Solution 2: Use a Virtual Machine (VM) that replicates everything over and over again.

Solution 3: Our friend Docker.

Docker creates containers for each application. Like giving each application their own room in an appartment. Another benefit of Docker is that you can copy any of those rooms and paste it into any other hotel that you want.

--example:

Fast, consistent delivery of your applications. Docker streamlines the development lifecycle by allowing developers to work in standardized environments using local containers which provide your applications and services.

Consider the following example scenario.

- Your developers write code locally and share their work with their colleagues using Docker containers

- They use Docker to push their applications into a test environment and execute automated and manual tests.

- When developers find bugs, they can fix them in the development environment and redeploy them to the test environment for testing and validation.

- When testing is complete, getting the fix to the customer is as simple as pushing the updated image to the production environment.

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

An image is a read-only template with instructions for creating a Docker container. Often, an image is based on another image, with some additional customization.

# Containers

Docker is an excellent platform to run software in containers. These containers are self-contained and isolated processes. A container is a runnable instance of an image. By default, a container is relatively well isolated from other containers and its host machine. You can control how isolated a container’s network, storage, or other underlying subsystems are from other containers or from the host machine.

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

# Docker VS Virtual Machine (VM)

Docker sounds a bit like a virtual machine, right?  It’s easy to connect those dots as both technologies share some characteristics. Both are designed to provide an isolated environment in which to run an application. Additionally, in both cases that environment can be moved between hosts. Docker is not a virtualization technology, it’s an application delivery technology. Virutal Machines are much larger because you have to install an Operating System, drivers, etc. for each VM instance. Think about it using this analogy: comparing houses (VMs) to apartment buildings (containers).

Houses (the VMs) are fully self-contained and offer protection from unwanted guests. They also each possess their own infrastructure – plumbing, heating, electrical, etc. Furthermore, in the vast majority of cases houses are all going to have at a minimum a bedroom, living area, bathroom, and kitchen. I’ve yet to ever find a “studio house” – even if I buy the smallest house I may end up buying more than I need because that’s just how houses are built.

Apartments (the containers) also offer protection from unwanted guests, but they are built around shared infrastructure. The apartment building (Docker Host) shares plumbing, heating, electrical, etc. Additionally apartments are offered in all kinds of different sizes – studio to multi-bedroom penthouse. You’re only renting exactly what you need.

Just like houses, apartments have front doors that lock to keep out unwanted guests.

With containers, you share the underlying resources of the Docker host and you build an image that is exactly what you need to run your application. You start with the basics and you add what you need.

VMs are built in the opposite direction. You are going to start with a full operating system and, depending on your application, might be strip out the things you don’t want.
