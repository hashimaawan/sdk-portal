# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlRhcmdldA

*This model accepts additional fields of type array.*


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `healthStatus` | [`?(HealthStatus[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/health-status.md) | Optional | - | getHealthStatus(): ?array | setHealthStatus(?array healthStatus): void |
| `server` | [`?Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-11.md) | Optional | - | getServer(): ?Server11 | setServer(?Server11 server): void |
| `type` | `?string` | Optional | - | getType(): ?string | setType(?string type): void |
| `usePrivateIp` | `?bool` | Optional | - | getUsePrivateIp(): ?bool | setUsePrivateIp(?bool usePrivateIp): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\TargetBuilder;
use HetznerCloudApiLib\Models\Builders\HealthStatusBuilder;
use HetznerCloudApiLib\Models\Status30;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Server11Builder;

$target = TargetBuilder::init()
    ->healthStatus(
        [
            HealthStatusBuilder::init()
                ->listenPort(142)
                ->status(Status30::UNKNOWN)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            HealthStatusBuilder::init()
                ->listenPort(142)
                ->status(Status30::UNKNOWN)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            HealthStatusBuilder::init()
                ->listenPort(142)
                ->status(Status30::UNKNOWN)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->server(
        Server11Builder::init(
            14
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->type('server')
    ->usePrivateIp(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



