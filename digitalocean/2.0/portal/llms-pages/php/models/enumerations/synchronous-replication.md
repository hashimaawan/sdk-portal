# Synchronous Replication

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN5bmNocm9ub3VzUmVwbGljYXRpb24

Synchronous replication type. Note that the service plan also needs to support synchronous replication.


# Enum Type Name

`SynchronousReplication`


# Fields

| Name |
|  --- |
| `OFF` |
| `QUORUM` |


# Example

```php
use DigitalOceanApiLib\Models\SynchronousReplication;

$synchronousReplication = SynchronousReplication::OFF;
```



