# Add Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFkZFN1Ym5ldFJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`AddSubnetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipRange` | `?string` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. If the Subnet is of type vSwitch, it also can not overlap with any gateway in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. | getIpRange(): ?string | setIpRange(?string ipRange): void |
| `networkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. | getNetworkZone(): string | setNetworkZone(string networkZone): void |
| `type` | [`string(Type42)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-42.md) | Required | Type of Subnetwork | getType(): string | setType(string type): void |
| `vswitchId` | `?int` | Optional | ID of the robot vSwitch. Must be supplied if the subnet is of type vswitch. | getVswitchId(): ?int | setVswitchId(?int vswitchId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\AddSubnetRequestBuilder;
use HetznerCloudApiLib\Models\Type42;
use HetznerCloudApiLib\ApiHelper;

$addSubnetRequest = AddSubnetRequestBuilder::init(
    'eu-central',
    Type42::SERVER
)
    ->ipRange('10.0.1.0/24')
    ->vswitchId(1000)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



