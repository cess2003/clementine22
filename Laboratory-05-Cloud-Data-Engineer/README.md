# Laboratory 05: The Cloud Data Engineer

## Mission Overview
In this mission, I worked as a Cloud Data Engineer at CloudNova Technologies. I researched the differences between block, file, and object storage, then deployed an S3-compatible MinIO object storage server using Docker on the KillerCoda Ubuntu Playground. I accessed the MinIO web console through port forwarding, created a private bucket named `client-photos`, and uploaded a test image to prove the system works.

## Objectives
- Differentiate between Block, File, and Object Storage
- Deploy an S3-compatible Object Storage server (MinIO) using Docker
- Access a cloud service through a web interface using port forwarding
- Create a storage bucket and upload objects (files) to the cloud
- Document cloud storage operations using Markdown
- Continue expanding my GitHub Cloud Computing Portfolio

## Tools Used
- KillerCoda Playground (Ubuntu)
- Docker
- MinIO (Chainguard `cgr.dev/chainguard/minio` image)
- MinIO web console (port 9001)
- GitHub
- Web browser

## Skills Learned
- Explaining the differences between block, file, and object storage
- Running a container with multiple port mappings and environment variables
- Accessing a containerized service through a forwarded port in the browser
- Creating a bucket and uploading objects in MinIO
- Reading error messages and fixing command problems
- Documenting technical steps clearly in Markdown

## Challenges Encountered
- **Multi-line command errors.** My first attempt at the `docker run` command failed with "`-e: command not found`" because I pasted the lines without the `\` line continuation characters. The shell treated each line as a separate command. I fixed it by entering the command as a single line.
- **Image no longer available.** The `minio/minio` image from the lab instructions returned `pull access denied` because MinIO removed it from Docker Hub. I solved it by using the Chainguard MinIO image (`cgr.dev/chainguard/minio`) with the same options, and the container ran successfully.
