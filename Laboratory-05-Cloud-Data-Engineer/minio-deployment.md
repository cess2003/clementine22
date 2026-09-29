# MinIO Deployment

This document will contain the technical steps used to deploy the MinIO S3-compatible object storage server using Docker.

## Docker Command
  docker rm -f minio-server
  docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
    -e "MINIO_ROOT_USER=cloudadmin" \
    -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
    pgsty/minio:RELEASE.2026-08-04T00-00-00Z server /data --console-address ":9001"

The MinIO server was deployed using Docker.

## Ports

- Port 9000 - MinIO API
- Port 9001 - MinIO Web Console

## Bucket

The bucket created for the activity is:

`client-photos`
