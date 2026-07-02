# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRlNuYXBzaG90cyUyRk92ZXJ2aWV3

[Snapshots](https://www.digitalocean.com/docs/images/snapshots/) are saved
instances of a Droplet or a block storage volume, which is reflected in
the `resource_type` attribute. In order to avoid problems with compressing
filesystems, each defines a `min_disk_size` attribute which is the minimum
size of the Droplet or volume disk when creating a new resource from the
saved snapshot.

To interact with snapshots, you will generally send requests to the
snapshots endpoint at `/v2/snapshots`.


# Get instance

An instance of the `SnapshotsApi` class can be accessed from the API Client.

```
SnapshotsApi snapshotsApi = client.SnapshotsApi;
```



