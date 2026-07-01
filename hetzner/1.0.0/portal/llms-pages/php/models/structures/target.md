# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlRhcmdldA


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `healthStatus` | [`?(HealthStatus[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/health-status.md) | Optional | - | getHealthStatus(): ?array | setHealthStatus(?array healthStatus): void |
| `server` | [`?Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-11.md) | Optional | - | getServer(): ?Server11 | setServer(?Server11 server): void |
| `type` | `?string` | Optional | - | getType(): ?string | setType(?string type): void |
| `usePrivateIp` | `?bool` | Optional | - | getUsePrivateIp(): ?bool | setUsePrivateIp(?bool usePrivateIp): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\TargetBuilder;
use HetznerCloudAPILib\Models\Builders\HealthStatusBuilder;
use HetznerCloudAPILib\Models\Status30Enum;
use HetznerCloudAPILib\Models\Builders\Server11Builder;

$target = TargetBuilder::init()
    ->healthStatus(
        [
            HealthStatusBuilder::init()
                ->listenPort(142)
                ->status(Status30Enum::UNKNOWN)
                ->build(),
            HealthStatusBuilder::init()
                ->listenPort(142)
                ->status(Status30Enum::UNKNOWN)
                ->build(),
            HealthStatusBuilder::init()
                ->listenPort(142)
                ->status(Status30Enum::UNKNOWN)
                ->build()
        ]
    )
    ->server(
        Server11Builder::init(
            14
        )->build()
    )
    ->type('server')
    ->usePrivateIp(false)
    ->build();
```



