# Laboratory 04: The Cloud-Native Engineer

## Mission Overview
In this mission, I took the role of a Cloud-Native Engineer at CloudNova Technologies. I compared Virtual Machines and Containers, then used Docker on KillerCoda to deploy, manage, and remove a containerized Nginx web server.

## Objectives
- Differentiate between Virtual Machines and Containers
- Access a Docker-enabled environment using KillerCoda
- Execute fundamental Docker CLI commands
- Pull, run, manage, and terminate an Nginx container
- Document container operations using Markdown
- Continue building my GitHub Cloud Computing Portfolio

## Docker Commands Executed
- `docker --version`
- `docker info`
- `docker pull nginx`
- `docker run -d -p 8080:80 --name my-nginx nginx`
- `curl http://localhost:8080`
- `docker ps`
- `docker stop my-nginx`
- `docker ps -a`
- `docker rm my-nginx`

## Skills Learned
- Explaining the difference between VMs and containers
- Pulling images and running containers in detached mode
- Mapping ports between host and container
- Managing the container lifecycle (run, stop, remove)
- Writing technical documentation in Markdown

## Challenges Encountered
(Isulat dito ang totoong naranasan mo. Halimbawa: nalito ako sa `-p 8080:80`, hindi ko alam ang pagkakaiba ng `docker ps` at `docker ps -a`, o natagalan akong mag-load ang KillerCoda.)
