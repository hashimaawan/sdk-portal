# Server 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlcjI

Configuration for type Server, required if type is `server`


# Class Name

`Server2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Server | getId(): int | setId(int id): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Server2Builder;

$server2 = Server2Builder::init(
    162
)->build();
```



