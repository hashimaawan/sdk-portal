# Subnet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlN1Ym5ldA

*This model accepts additional fields of type array.*


# Class Name

`Subnet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `gateway` | `string` | Required | Gateway for Servers attached to this subnet. For subnets of type Server this is always the first IP of the network IP range. | getGateway(): string | setGateway(string gateway): void |
| `ipRange` | `?string` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. | getIpRange(): ?string | setIpRange(?string ipRange): void |
| `networkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. | getNetworkZone(): string | setNetworkZone(string networkZone): void |
| `type` | [`string(Type42)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-42.md) | Required | Type of Subnetwork | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\SubnetBuilder;
use HetznerCloudApiLib\Models\Type42;
use HetznerCloudApiLib\ApiHelper;

$subnet = SubnetBuilder::init(
    '10.0.0.1',
    'eu-central',
    Type42::SERVER
)
    ->ipRange('10.0.1.0/24')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



