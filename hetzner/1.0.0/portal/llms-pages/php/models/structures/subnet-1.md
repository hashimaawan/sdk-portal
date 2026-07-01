# Subnet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlN1Ym5ldDE

*This model accepts additional fields of type array.*


# Class Name

`Subnet1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipRange` | `?string` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. | getIpRange(): ?string | setIpRange(?string ipRange): void |
| `networkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. | getNetworkZone(): string | setNetworkZone(string networkZone): void |
| `type` | [`string(Type42)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-42.md) | Required | Type of Subnetwork | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Subnet1Builder;
use HetznerCloudApiLib\Models\Type42;
use HetznerCloudApiLib\ApiHelper;

$subnet1 = Subnet1Builder::init(
    'eu-central',
    Type42::VSWITCH
)
    ->ipRange('10.0.1.0/24')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



