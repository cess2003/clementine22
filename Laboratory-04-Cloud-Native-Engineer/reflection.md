Mission Reflection

1. Boot time and setup compared to a VM.
A Docker container starts in seconds, while a Virtual Machine takes minutes because it must install and boot a full operating system. Setting up Nginx in a VM would mean installing the OS, updating packages, installing the web server, and configuring it. With Docker, I only needed two commands: docker pull and docker run. This showed me how much faster and simpler containers are.

2. Why port mapping is necessary.
A container has its own isolated network, so the web server listening on port 80 inside it is not reachable from the host by default. Port mapping with -p 8080:80 connects port 8080 on the host to port 80 in the container. Without it, I could not access Nginx using curl http://localhost:8080.

3. What happens to data after docker rm.
When a container is removed with docker rm, its writable layer is deleted, so any data stored inside is lost permanently. To keep data, you need volumes or bind mounts, which store it outside the container.

4. Containers and DevOps.
Containers package an application with everything it needs, so developers and operations teams work in the same environment. This reduces the “it works on my machine” problem. Developers can ship consistent images, and operations teams can deploy and scale them easily, which makes collaboration, testing, and automation smoother.

5. How my portfolio is evolving.
My GitHub portfolio now has several labs, each with its own folder, documentation, and screenshots. I am getting better at writing Markdown, organizing repositories, and committing regularly. It is slowly becoming a record of my skills in cloud computing, from cloud providers to containers.
