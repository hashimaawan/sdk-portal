# Protocol 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlByb3RvY29sMQ

The protocol used for health checks sent to the backend Droplets. The possible values are `http`, `https`, or `tcp`.


# Enum Type Name

`Protocol1`


# Fields

| Name |
|  --- |
| `HTTP` |
| `HTTPS` |
| `TCP` |


# Example

```php
use DigitalOceanApiLib\Models\Protocol1;

$protocol1 = Protocol1::HTTP;
```



