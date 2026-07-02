# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkJsb2NrJTI1MjBTdG9yYWdlJTJGT3ZlcnZpZXc

[DigitalOcean Block Storage Volumes](https://www.digitalocean.com/docs/volumes/)
provide expanded storage capacity for your Droplets and can be moved
between Droplets within a specific region.

Volumes function as raw block devices, meaning they appear to the
operating system as locally attached storage which can be formatted using
any file system supported by the OS. They may be created in sizes from
1GiB to 16TiB.

By sending requests to the `/v2/volumes` endpoint, you can list, create, or
delete volumes as well as attach and detach them from Droplets


# Get singleton instance

The singleton instance of the `BlockStorageApi` class can be accessed from the API Client.

```
$blockStorageApi = $client->getBlockStorageApi();
```



