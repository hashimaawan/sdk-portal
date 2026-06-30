# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Server from being deleted | getDelete(): bool | setDelete(bool delete): void |
| `rebuild` | `bool` | Required | If true, prevents the Server from being rebuilt | getRebuild(): bool | setRebuild(bool rebuild): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Protection20Builder;

$protection20 = Protection20Builder::init(
    false,
    false
)->build();
```



