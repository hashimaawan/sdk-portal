# Server 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcjk

Configuration for type server, required if type is `server`


# Class Name

`Server9`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Server | getId(): int | setId(int id): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Server9Builder;

$server9 = Server9Builder::init(
    216
)->build();
```



