# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRlNpemVzJTJGT3ZlcnZpZXc

The sizes objects represent different packages of hardware resources that
can be used for Droplets. When a Droplet is created, a size must be
selected so that the correct resources can be allocated.

Each size represents a plan that bundles together specific sets of
resources. This includes the amount of RAM, the number of virtual CPUs,
disk space, and transfer. The size object also includes the pricing
details and the regions that the size is available in.


# Create Instance

The instance of the `SizesApi` class can be created using the API Client.

```
const sizesApi = new SizesApi(client);
```



