# Synchronous Replication

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlN5bmNocm9ub3VzUmVwbGljYXRpb24

Synchronous replication type. Note that the service plan also needs to support synchronous replication.


# Enum Type Name

`SynchronousReplication`


# Fields

| Name |
|  --- |
| `OFF` |
| `QUORUM` |


# Example

```python
from digitaloceanapi.models.synchronous_replication import SynchronousReplication

synchronous_replication = SynchronousReplication.OFF
```



