# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `listenPort` | `?int` | Optional | - | getListenPort(): ?int | setListenPort(?int listenPort): void |
| `status` | [`?string(Status30Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/status-30.md) | Optional | - | getStatus(): ?string | setStatus(?string status): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\HealthStatusBuilder;
use HetznerCloudAPILib\Models\Status30Enum;

$healthStatus = HealthStatusBuilder::init()
    ->listenPort(443)
    ->status(Status30Enum::HEALTHY)
    ->build();
```



