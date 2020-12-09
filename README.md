# minio-vorteil

A simple implementation of [MinIO](https://min.io/) on AWS using AWS EFS (Elastic File Services) as the backend for the MinIO server and the server running on [Vorteil Open Source](https://github.com/vorteil/vorteil)

## Description

This repository contains the Vorteil machine configuration for the Medium article:

https://medium.com/@wilhelm-wonigkeit/minio-on-vorteil-s3-api-nfs-access-on-aws-aa45336abfc6

This package contains the Vorteil configuration files and the MinIO binary. The binary can be updated using the following commmand:

```wget https://dl.min.io/server/minio/release/linux-amd64/minio```


## Using the Vorteil machine configuration

1. Download and install the latest [Vorteil open source toolkit](https://github.com/vorteil/vorteil)
2. Clone the repo to an appropriate directory on your local machine
3. If you want to use NFS:
       
   - map the correct NFS shares (IP address & mount points) in the default.vcfg configuration file
   
   or, if you only want to use local disk:
       
   - just remove the configuration for NFS completely
       
4. Run the machine using `vorteil run <cloned-directory>` or provision using `vcli images provision <directory> <provisioner> --name minio --system.hostname minio`

If you have any questions just ask!
