# State

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXRl

A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`.


# Enum Type Name

`State`


# Fields

| Name |
|  --- |
| `PENDING` |
| `VERIFIED` |
| `ERROR` |


# Example

```php
use DigitalOceanApiLib\Models\State;

$state = State::ERROR;
```



