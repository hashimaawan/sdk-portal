# State 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXRlMg

A string indicating the current status of the cluster.


# Enum Type Name

`State2`


# Fields

| Name |
|  --- |
| `RUNNING` |
| `PROVISIONING` |
| `DEGRADED` |
| `ERROR` |
| `DELETED` |
| `UPGRADING` |
| `DELETING` |


# Example

```php
use DigitalOceanApiLib\Models\State2;

$state2 = State2::DELETING;
```



