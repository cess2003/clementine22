# Laboratory 03 – Multi-Cloud Explorer

## Introduction

This laboratory is about exploring and comparing three major cloud platforms: Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP). I researched their services, advantages, infrastructure, and possible uses for different organizations.

## Objectives

The objectives of this laboratory are:

* To explore AWS, Azure, and Google Cloud.
* To identify important cloud services.
* To compare services from different cloud providers.
* To recommend cloud platforms for different business situations.
* To investigate a Linux server using KillerCoda.
* To improve my Cloud Computing Portfolio using Markdown.

## Linux Server Investigation

I used a KillerCoda Playground to investigate a Linux server.

### Operating System

The operating system of the server is:
Ubuntu Linux
Command used:
cat /etc/os-release | grep PRETTY_NAME

```bash
cat /etc/os-release
```

### CPU Information

The CPU information is:
CPU: 2 CPUs
Command used:
lscpu | grep -E 'Model name|CPU\(s\)' | head -2
```bash
lscpu
```

### Memory

The memory information is:
lscpu | grep -E 'Model name|CPU\(s\)' | head -2
Command used:
free -h
```bash
free -h
```

### Disk Space

The disk space information is:
Approximately 30 GiB total disk space
Command used:

```bash
df -h
```

## Cloud Migration

If this Linux server were moved to the cloud, it could be hosted by any of the three major cloud providers.

| Cloud Provider  | Service That Can Host the Linux Server |
| --------------- | -------------------------------------- |
| AWS             | Amazon EC2                             |
| Microsoft Azure | Azure Virtual Machines                 |
| Google Cloud    | Compute Engine                         |

These services provide virtual machines where Linux operating systems and applications can be installed and operated.

## Screenshots

### AWS

![AWS Homepage](screenshots/aws-homepage.png)

### Azure

![Azure Homepage](screenshots/azure-homepage.png)

### Google Cloud

![Google Cloud Homepage](screenshots/gcp-homepage.png)

### KillerCoda

![KillerCoda Terminal](screenshots/killercoda-terminal.png)

## Conclusion

After comparing AWS, Azure, and Google Cloud, I learned that all three providers offer similar basic cloud services, but each one has different strengths. AWS has a very wide range of services, Azure is a good option for organizations using Microsoft technologies, and Google Cloud is especially strong in artificial intelligence, machine learning, data analytics, and Kubernetes.
