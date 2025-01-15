# Docker in 100s

Docker is a tool that can package software into containers that run reliably in any environment. 

![alt text](images/{CA56502A-A841-4789-A8C6-B6F311073387}.png)

**But what is a container and why do you need one?** 

![alt text](images/{57A72B31-5B28-40B3-93FF-7792B45972B3}.png)

Imagine you built an app with Cobol that runs on some weird flavour of linux. You want to share this app with your friend, but he has an entirely different system. 

![alt text](images/{05951731-C595-4E09-9378-AAA8B41F48B1}.png)

**So, the problem becomes:** how do we replicate the environment our software needs on *any* machine?

One way to package an app is with a **virtual machine**, where the hardware is simulated, then installed with the required OS and dependencies. 

![alt text](images/{9C4A9FDF-B1BB-45CC-92C7-2700ABFE074F}.png)

This approach allows you to run multiple apps on the same infrastructure, however because each vm is running its own operating system they tend to be bulky and slow - like an overweight cat trying to make its way through a small cat flap. 

![alt text](images/{7B64F9D6-8533-40C6-BFB5-285D65AE0D35}.png)

<br>

### Docker container similar to a vm - but better! 

A docker container is conceptually very simiar to a vm - **with one key difference!** Instead of virtualizing hardware, containers *only virtualize the OS*. 

![alt text](images/{9E5213D6-0E3C-4A99-9BAC-342AE96F9F13}.png)

In other words, all apps or containers are run by a single kernel - and this makes everything faster and more efficient. 

![alt text](images/{3B64EF8B-F5E1-41C5-9E88-F92DCB8258ED}.png)

<br><br>

### 3 fundamental elements in the Docker universe

![alt text](images/{29A63D76-3D7E-4F7D-A848-A980E83B3D30}.png)

![alt text](images/{A39F1156-E713-4017-9EC2-A9D9A2A70220}.png)

#### Dockerfile

The dockerfile is like DNA. It's just code that tells docker how to build an image.

![alt text](images/{B0878BE8-28DD-4B7E-AD85-AB91C2D804AD}.png)

#### Image

An image in docker is just a snapshot of your software, along with all its dependencies - down to the OS level. 

![alt text](images/{72A505E1-670C-48A4-8F37-08F9BBB4EDA5}.png)

#### Container

The image is **immutable**, and it can be used to spin up multiple containers, which is your actual software running in the real world. 

![alt text](images/{29E25749-F861-4556-9300-ED6637F19699}.png)

<br>

### Getting Started - FROM

Create a docker file and use `FROM` to start from an existing template like ubuntu. 

![alt text]({DABBCE39-3DE8-47CF-9C75-A938DE2987DD}.png)

This base image gets pulled down from the cloud, and you can also upload your own images to a variety of different docker registries. 

![alt text]({852CD949-0F2C-4EE0-A5E8-01E324F7B54E}.png)

<br>

### Getting Started - RUN

From there, you might want to use `RUN` to run a terminal command that installs dependencies into your image. 

![alt text]({94274763-1C0A-452F-98BC-27160CCF39E7}.png)

<br>

### ENV Variables 

You can set environment variables and do all kinds of other stuff. 

![alt text]({15665CD5-F2B8-40B0-9518-3860367BF39F}.png)


### CMD 

The last thing you'll do is set a default command `CMD` that's executed when you start up a container.

![alt text]({BDF82976-B552-4FDF-9EDB-01818C08219A}.png)

<br>

### `docker build` command

Then you can create the image file, by running the `docker build` command. It goes through each step in our docker file to build the image layer by layer. 

![alt text]({9061E48D-39EA-4CE1-8B32-7B9CA4C54876}.png)

### `docker run` command

We can then bring this image to life as a container with the `docker run` command. 

![alt text]({8C0D668D-C59A-4EBC-8E5A-A2C799625244}.png)

<br>

As your app demands more resources you can run it on multiple machines, multiple clouds, on-premises (installed on own hardware) - or wherever you want reliably. 

![alt text]({AF5362ED-7E2C-4D3B-8576-87F5583074F9}.png)

