# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlVzZWRCeQ


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | ID of resource referenced | getId(): int | setId(int id): void |
| `type` | `string` | Required | Type of resource referenced | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\UsedByBuilder;

$usedBy = UsedByBuilder::init(
    4711,
    'load_balancer'
)->build();
```



