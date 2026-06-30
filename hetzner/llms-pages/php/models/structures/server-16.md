# Server 16

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlcjE2

Configuration for type Server, required if type is `server`


# Class Name

`Server16`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `float` | Required | ID of the Server | getId(): float | setId(float id): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Server16Builder;

$server16 = Server16Builder::init(
    80
)->build();
```



