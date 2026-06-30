# Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlcg


# Class Name

`Server`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServerBuilder;

$server = ServerBuilder::init(
    42
)->build();
```



