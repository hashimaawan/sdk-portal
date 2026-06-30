# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlJlc291cmNl


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `type` | `string` | Required | Type of resource referenced | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Resource2Builder;

$resource = Resource2Builder::init(
    42,
    'server'
)->build();
```



