# Status 15

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXR1czE1

The current status of this garbage collection.


# Enum Type Name

`Status15`


# Fields

| Name |
|  --- |
| `REQUESTED` |
| `ENUM_WAITING_FOR_WRITE_JWTS_TO_EXPIRE` |
| `ENUM_SCANNING_MANIFESTS` |
| `ENUM_DELETING_UNREFERENCED_BLOBS` |
| `CANCELLING` |
| `FAILED` |
| `SUCCEEDED` |
| `CANCELLED` |


# Example

```php
use DigitalOceanApiLib\Models\Status15;

$status15 = Status15::CANCELLING;
```



