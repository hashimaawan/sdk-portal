# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkRhdGFjZW50ZXJzJTJGT3ZlcnZpZXc

Each Datacenter represents a *virtual* Datacenter which is made up of possible many physical Datacenters where Servers are hosted.

Datacenter names are composed from their Location and virtual Datacenter number, for example `fsn1-dc14` means virtual Datacenter `14` in Location `fsn1`.

Right now there is only one Datacenter for each Location. The Datacenter numbers for `fsn`, `nbg` and `hel` are arbitrarily set to `14`, `3` and `2` for historic reasons and do not represent real physical Hetzner datacenters.


# Get instance

An instance of the `DatacentersApi` class can be accessed from the API Client.

```
datacenters_api = client.datacenters
```



