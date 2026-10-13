# Mission Reflection

**1. Why object storage is better suited for millions of photos than block storage.**
Object storage is better suited for millions of photos because it stores each file as an independent object with its own metadata and unique ID in a flat structure, so it can scale almost without limit by adding more servers. A block storage drive is attached to a single machine and has a fixed size, so it becomes expensive and hard to manage as data grows. Object storage is also cheaper per gigabyte and can be reached from anywhere over HTTP.

**2. How Docker made it easier to deploy MinIO.**
Docker made deployment much easier because I did not have to install or configure MinIO by hand. One `docker run` command pulled the image, started the server, opened ports 9000 and 9001, and set the login credentials through environment variables. When the original image was no longer available, I only had to change the image name, and the rest of the command still worked.

**3. What a bucket is.**
A bucket is a top-level container in object storage that holds objects (files). It is similar to a folder, but it has a unique name and its own access policy. In this lab, `client-photos` was the private bucket where I uploaded my test image.

**4. How enterprises prevent data loss when a server crashes.**
Large companies replicate data across many drives, servers, and data centers in different regions, so a single crash does not cause data loss. Many systems also use erasure coding, which splits data into pieces with parity so missing pieces can be rebuilt. Versioning and backups add another layer of protection.

**5. Growing confidence in the Linux command line.**
My confidence is growing. My first attempt failed because I pasted a multi-line command without backslashes, and the image I needed was no longer available. By reading the error messages, fixing the command, and checking the results with `docker ps`, I solved both problems. Each lab makes the terminal feel less intimidating.
