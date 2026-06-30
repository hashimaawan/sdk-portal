# Protection 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByb3RlY3Rpb24xMQ

Protection configuration for the Network


# Class Name

`Protection11`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Network from being deleted | getDelete(): bool | setDelete(bool delete): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Protection11Builder;

$protection11 = Protection11Builder::init(
    false
)->build();
```



