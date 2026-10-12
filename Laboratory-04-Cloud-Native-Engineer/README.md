# Laboratory 04: The Cloud-Native Engineer

## Mission Overview
In this mission, I worked as a Cloud-Native Engineer at CloudNova Technologies. I researched the differences between Virtual Machines and Containers, then used the KillerCoda Ubuntu playground to deploy a containerized Nginx web server with Docker. I also managed the container through its full lifecycle: running, stopping, and removing it. All commands and results are documented in this folder.

## Objectives
- Differentiate between Virtual Machines and Containers
- Access a Docker-enabled cloud environment using KillerCoda
- Execute fundamental Docker CLI commands
- Pull, run, manage, and terminate a containerized application (Nginx)
- Create technical documentation of container operations using Markdown
- Continue developing my GitHub Cloud Computing Portfolio

## Docker Commands Executed

### Checkpoint 3: Verifying Docker
- `docker --version`
- `docker info`

### Checkpoint 4: Deploying Nginx
- `docker pull nginx`
- `docker run -d -p 8080:80 --name my-nginx nginx`
- `curl http://localhost:8080`

### Checkpoint 5: Container Lifecycle
- `docker ps`
- `docker stop my-nginx`
- `docker ps -a`
- `docker rm my-nginx`

## Skills Learned
- Explaining how containers share the host OS while VMs each run a full guest OS
- Verifying that Docker is installed and running in a Linux environment
- Pulling images from Docker Hub and running containers in detached mode
- Using port mapping to make a containerized web server reachable from the host
- Managing a container's lifecycle with `docker ps`, `docker stop`, and `docker rm`
- Writing clear technical documentation in Markdown and organizing it in a GitHub repository

## Challenges Encountered
- **Understanding port mapping.** At first I was confused by `-p 8080:80`. I didn't understand why there were two port numbers. I learned that the first number is the port on the host and the second is the port inside the container, so Nginx on port 80 inside the container is reached through port 8080 on the host.
- **Telling `docker ps` and `docker ps -a` apart.** After stopping the container, `docker ps` showed nothing, and I thought it had disappeared. I then learned that `docker ps -a` shows stopped containers too, which is how I confirmed it had exited before removing it.
- **Taking screenshots in the playground.** The KillerCoda terminal fills up quickly, so some of my commands scrolled out of view. I used `clear` before each step so the output fit in a single screenshot.
- **Creating folders on GitHub.** The GitHub website has no "New folder" button, so I had to type the folder name followed by `/` in the filename box when creating a new file.
