# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ

*This model accepts additional fields of type array.*


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ip` | `?string` | Optional | - | getIp(): ?string | setIp(?string ip): void |
| `network` | `?int` | Optional | - | getNetwork(): ?int | setNetwork(?int network): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PrivateNetBuilder;
use HetznerCloudApiLib\ApiHelper;

$privateNet = PrivateNetBuilder::init()
    ->ip('10.0.0.2')
    ->network(4711)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



