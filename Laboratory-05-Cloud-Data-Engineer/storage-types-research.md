# Types of Cloud Storage

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|--------------|-------------|------------------|------------------------|
| **Block Storage** | Splits data into fixed-size blocks stored on a volume attached to a single server, like a virtual hard drive. | Operating systems, databases, and applications that need fast, low-latency disk access. | AWS EBS |
| **File Storage** | Stores data as files in a hierarchy of folders and directories that multiple servers can share over a network. | Shared drives, home directories, and content that several users or servers access at the same time. | AWS EFS |
| **Object Storage** | Stores data as objects in a flat structure, each with its own metadata and unique ID, accessed over HTTP/API. | Images, videos, backups, logs, and other large amounts of unstructured data. | AWS S3 |

## Recommendation for the Client

Object Storage is the best choice for the client's user-uploaded images because it can scale to millions of files without a fixed size limit or complicated folder management. It is also cost-effective and accessible from anywhere over the web, so the photo-sharing application can store and retrieve images directly. Unlike a container, the data stays safe and persistent even if the web server is replaced or restarted.
