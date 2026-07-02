# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkRhdGFiYXNlcyUyRk92ZXJ2aWV3

DigitalOcean's [managed database service](https://www.digitalocean.com/docs/databases)
simplifies the creation and management of highly available database clusters. Currently, it
offers support for [PostgreSQL](http://www.digitalocean.com/docs/databases/postgresql/),
[Redis](https://www.digitalocean.com/docs/databases/redis/),
[MySQL](https://www.digitalocean.com/docs/databases/mysql/), and
[MongoDB](https://www.digitalocean.com/docs/databases/mongodb/).

By sending requests to the `/v2/databases` endpoint, you can list, create, or delete
database clusters as well as scale the size of a cluster, add or remove read-only replicas,
and manage other configuration details.

Database clusters may be deployed in a multi-node, high-availability configuration.
If your machine type is above the basic nodes, your node plan is above the smallest option,
or you are running MongoDB, you may additionally include up to two standby nodes in your cluster.

The size of individual nodes in a database cluster is represented by a human-readable slug,
which is used in some of the following requests. Each slug denotes the node's identifier,
CPU count, and amount of RAM, in that order.

For **Basic nodes**, reference the following table for its slug:

Slug               | CPU     | RAM
-------------------|---------|---------
db-s-1vcpu-1gb     | 1 vCPU  | 1 GB
db-s-1vcpu-2gb     | 1 vCPU  | 2 GB
db-s-2vcpu-4gb     | 2 vCPU  | 4 GB
db-s-4vcpu-8gb     | 4 vCPU  | 8 GB
db-s-6vcpu-16gb    | 6 vCPU  | 16 GB
db-s-8vcpu-32gb    | 8 vCPU  | 32 GB
db-s-16vcpu-64gb   | 16 vCPU | 64 GB

For **General Purpose nodes**, reference the following table for its slug:

Slug               | CPU     | RAM
-------------------|---------|---------
gd-2vcpu-8gb       | 2 vCPU  | 8 GB
gd-4vcpu-16gb      | 4 vCPU  | 16 GB
gd-8vcpu-32gb      | 8 vCPU  | 32 GB
gd-16vcpu-64gb     | 16 vCPU | 64 GB
gd-32vcpu-128gb    | 32 vCPU | 128 GB
gd-40vcpu-160gb    | 40 vCPU | 160 GB

For **Storage-Optimized nodes**, reference the following table for its slug:

Slug               | CPU     | RAM
-------------------|---------|---------
so1_5-2vcpu-16gb   | 2 vCPU  | 16 GB
so1_5-4vcpu-32gb   | 4 vCPU  | 32 GB
so1_5-8vcpu-64gb   | 8 vCPU  | 64 GB
so1_5-16vcpu-128gb | 16 vCPU | 128 GB
so1_5-24vcpu-192gb | 24 vCPU | 192 GB
so1_5-32vcpu-256gb | 32 vCPU | 256 GB

For **Memory-Optimized nodes**, reference the following table for its slug:

Slug               | CPU     | RAM
-------------------|---------|---------
m-2vcpu-16gb       | 2 vCPU  | 16 GB
m-4vcpu-32gb       | 4 vCPU  | 32 GB
m-8vcpu-64gb       | 8 vCPU  | 64 GB
m-16vcpu-128gb     | 16 vCPU | 128 GB
m-24vcpu-192gb     | 24 vCPU | 192 GB
m-32vcpu-256gb     | 32 vCPU | 256 GB


# Get instance

An instance of the `DatabasesApi` class can be accessed from the API Client.

```
databases_api = client.databases
```



