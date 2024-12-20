# Dockerized Web Application

![Docker Logo](https://blog.ippon.tech/hubfs/Imported_Blog_Media/docker_logo-Jan-18-2024-06-04-17-8544-PM.png)

This project is designed as a school exercise to create a fully Dockerized web application. Through a series of tasks, we gradually build a system that includes both front-end and back-end components, along with Docker Compose for easier management, and a load-balancing setup for scaling.

## Index

0. [Create Your First Docker Image](#0-create-your-first-docker-image)
1. [Back-end Setup](#1-back-end-setup)
2. [Front-end Setup](#2-front-end-setup)
3. [Connecting the Front-end and Back-end](#3-connecting-the-front-end-and-back-end)
4. [Making it Simpler with Docker Compose](#4-making-it-simpler-with-docker-compose)
5. [Proxy Server](#5-proxy-server)
6. [Scale Horizontally](#6-scale-horizontally)

---

## 0. Create Your First Docker Image

**Task Description:**

For this first task, you need to create a Docker image using a Dockerfile that:

- Is based on the latest Ubuntu image.
- Updates APT using `apt-get update`.
- Upgrades currently installed software using `apt-get upgrade -y`.

Once built, the Docker container should print "Hello, World!" when executed.

---

## 1. Back-end Setup

**Task Description:**

For this task, start by copying the `task0` directory and renaming it `task1`. Then, modify the Dockerfile to:

- Install Python3, pip3, and Flask.

You’ll validate the setup by running a Flask server with one endpoint that returns "Hello, World!" when accessed.

---

## 2. Front-end Setup

**Task Description:**

Start by copying the `task1` directory and renaming it `task2`. In this task, you will:

- Reorganize the project structure.
- Create a basic front-end that interacts with your API server.

---

## 3. Connecting the Front-end and Back-end

**Task Description:**

Copy the `task2` directory and rename it `task3`. In this task, you’ll:

- Connect the front-end to the back-end, allowing dynamic data exchange.
- Ensure communication between the two Docker containers (one for the front-end and one for the back-end).

---

## 4. Making it Simpler with Docker Compose

**Task Description:**

Copy the `task3` directory and rename it `task4`. In this task, you’ll:

- Create a `docker-compose.yml` file that manages both the front-end and back-end containers.
- Use Docker Compose to spin up your entire application with a single command.

---

## 5. Proxy Server

**Task Description:**

Copy the `task4` directory and rename it `task5`. In this task, you’ll:

- Set up a proxy server using Nginx to route traffic between the front-end and back-end.
- Create a new folder named `proxy` containing:
  - A Dockerfile based on the latest Nginx image.
  - A `proxy.conf` file that handles routing.

The proxy server will:

- Route requests to `/` to the front-end container.
- Route requests to `/api` to the back-end container.

---

## 6. Scale Horizontally

**Task Description:**

Copy the `task5` directory and rename it `task6`. In this task, you’ll:

- Launch multiple instances of the back-end API server to handle increased traffic.
- Configure Nginx for load balancing using a Round-Robin strategy between the API servers.

---
