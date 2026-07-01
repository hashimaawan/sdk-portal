# Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlR5cGUx

Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`.


# Enum Type Name

`Type1`


# Fields

| Name |
|  --- |
| `UPLOADED` |
| `MANAGED` |


# Example

```php
use HetznerCloudApiLib\Models\Type1;

$type1 = Type1::UPLOADED;
```



