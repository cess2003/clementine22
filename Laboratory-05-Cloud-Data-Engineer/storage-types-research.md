# Storage Types Research

Cloud storage can be divided into three primary types: Block Storage, File Storage, and Object Storage. Each type stores and organizes data differently and is designed for different workloads.

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| **Block Storage** | Stores data in fixed-size blocks that can be managed by an operating system like a virtual hard drive. | Best for virtual machines, databases, and applications that require fast and consistent disk access. | AWS Elastic Block Store (EBS) |
| **File Storage** | Stores data as files organized in folders and directories. Multiple systems can access the same file storage through a network. | Best for shared folders, file-based applications, and shared documents. | AWS Elastic File System (EFS) |
| **Object Storage** | Stores data as objects together with metadata and a unique identifier inside containers called buckets. | Best for large amounts of unstructured data such as images, videos, backups, and documents. | Amazon Simple Storage Service (S3) |

## Why Object Storage Is Best for the Client

Object Storage is well suited for the client's photo-sharing application because it is designed to store large amounts of unstructured data such as user-uploaded images. It can organize large numbers of files into buckets and allows applications to access objects without depending on a traditional server's local hard drive.
