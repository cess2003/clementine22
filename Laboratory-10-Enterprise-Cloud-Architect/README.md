# Project Overview

For our final laboratory project, our group designed and deployed a private cloud storage system using Nextcloud and MariaDB. The main goal of this project was to understand how different components of a cloud environment work together, including virtual machine configuration, network setup, application deployment, and database integration.

We used Ubuntu Server as our operating system and Docker Compose to manage the application and database services. We also configured a firewall to strengthen network security and developed an automated database backup script to support data protection and system maintenance.

# Project Objectives

- Deploy Nextcloud as a private cloud storage application.
- Connect Nextcloud to a MariaDB database using Docker Compose.
- Implement persistent Docker volumes to ensure data is retained.
- Configure a firewall to control and secure incoming network connections.
- Automate database backups using a Bash script and cron.
- Document the system architecture, deployment process, security configurations, and maintenance procedures.

# Technology Stack

- **Operating System:** Ubuntu Server
- **Virtualization:** Oracle VirtualBox
- **Container Platform:** Docker
- **Container Management:** Docker Compose
- **Cloud Storage Application:** Nextcloud
- **Database Management System:** MariaDB
- **Firewall:** UFW
- **Automation Tools:** Bash and cron
- **Source Code Repository:** GitHub

# Project Files

| File | Description |
|---|---|
| `README.md` | Contains the project overview, objectives, and technology stack. |
| `architecture-diagram.png` | Illustrates the system architecture and network topology. |
| `docker-compose.yml` | Contains the configuration for the Nextcloud and MariaDB containers. |
| `automation-script.sh` | Contains the script used to perform automated database backups. |
| `operational-manual.md` | Documents the deployment, security, maintenance, and troubleshooting procedures. |
| `final-reflection.md` | Presents our group's reflections and learning experiences throughout the cloud computing activities. |

# Security and Data Persistence

Our deployment uses environment variables to manage sensitive configuration settings and persistent Docker volumes to ensure that application and database data remain available even after containers are restarted or recreated.

We also configured UFW (Uncomplicated Firewall) to deny incoming connections by default while allowing only the necessary ports for SSH and web access.

To improve data protection, we developed an automated database backup script that generates compressed backup files, records backup results in a log file, and automatically removes older backups based on the configured retention period.

For security purposes, the `.env` file contains sensitive credentials and must not be committed or uploaded to the public GitHub repository.

# Learning Outcomes

Through this project, our group gained practical experience in container deployment, database connectivity, network security, persistent storage, and automated backup management. We also developed a better understanding of how different cloud computing components work together to provide a functional and secure cloud environment.

Furthermore, this activity taught us the importance of proper system documentation, regular maintenance, and data protection in managing a cloud infrastructure.

# Deployment Verification

The deployment was successfully tested on Ubuntu Server using Docker Compose. Both the Nextcloud application and MariaDB database containers were confirmed to be running properly.

We accessed the Nextcloud login page through a web browser on the Windows host machine and verified that previously uploaded files remained accessible after restarting the application container.

We also checked the persistent Docker volumes, verified the UFW firewall rules, and tested the generated database backup archive. The backup log successfully recorded the backup operations, and cron was configured to execute the backup script daily at 2:00 AM based on the Ubuntu system time.

These verification steps confirmed that the main components of our private cloud storage system were functioning as expected.
