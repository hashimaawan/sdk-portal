# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource


# Class Name

`Protection`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Resource from being deleted | getDelete(): bool | setDelete(bool delete): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;

$protection = ProtectionBuilder::init(
    false
)->build();
```



