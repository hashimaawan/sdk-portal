# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw

*This model accepts additional fields of type array.*


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `listenPort` | `?int` | Optional | - | getListenPort(): ?int | setListenPort(?int listenPort): void |
| `status` | [`?string(Status30)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/status-30.md) | Optional | - | getStatus(): ?string | setStatus(?string status): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\HealthStatusBuilder;
use HetznerCloudApiLib\Models\Status30;
use HetznerCloudApiLib\ApiHelper;

$healthStatus = HealthStatusBuilder::init()
    ->listenPort(443)
    ->status(Status30::HEALTHY)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



