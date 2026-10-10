Mission Reflection

Preparing a docker-compose.yml file makes the job of a cloud engineer easier since the
whole environment is described in one readable file instead of several long
The commands; in Mission 4 each docker run command required its ports, variables, and
Names were typed by hand, and a single typo required starting again. With Compose, I wrote the
We generated the blueprint at one time and started both containers with a single command. The file can
also be saved to GitHub, reviewed, shared, and reused, so deployments stay
consistent and repeatable.

YAML uses indentation to display its structure; if I use a tab rather than spaces,
If a line is misaligned, Docker Compose will not be able to parse the file and will display an error. A
misaligned key could also be read as belonging to the wrong service, so the stack
could fail to deploy or function incorrectly.

We used environment variables like MYSQL_PASSWORD so that settings are passed into
When the containers are started, rather than having them built into the image, this allows
the same image be reused with different configurations and ensures the database
and the app uses the same credentials. In actual production, secrets would be
It should be kept in a .env file or in a secrets manager and not written in plain text.

Deploying Nextcloud, a full private cloud storage platform, in just a few minutes
felt great. Software which would take hours to install by hand was running with
a single command together with approximately twenty lines of code; I also made a mistake at some point: I
pasted the YAML into the terminal instead of nano, and every line returned
"command not found". That fact showed me that both the editor and the sequence of steps really
matter.

My grasp of cloud computing has changed a great deal since Mission 1. I used to
Imagine it just as a way of storing files online; now I view it as being able to provide them when needed.
infrastructure that can be automated, defined as code, and deployed quickly using
Things such as Docker and Compose. I also know how containers, networking, and
The documentation fits together when used in actual deployments.
