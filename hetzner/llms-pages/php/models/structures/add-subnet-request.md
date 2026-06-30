# Add Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkFkZFN1Ym5ldFJlcXVlc3Q


# Class Name

`AddSubnetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipRange` | `?string` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. If the Subnet is of type vSwitch, it also can not overlap with any gateway in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. | getIpRange(): ?string | setIpRange(?string ipRange): void |
| `networkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. | getNetworkZone(): string | setNetworkZone(string networkZone): void |
| `type` | [`string(Type42Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-42.md) | Required | Type of Subnetwork | getType(): string | setType(string type): void |
| `vswitchId` | `?int` | Optional | ID of the robot vSwitch. Must be supplied if the subnet is of type vswitch. | getVswitchId(): ?int | setVswitchId(?int vswitchId): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\AddSubnetRequestBuilder;
use HetznerCloudAPILib\Models\Type42Enum;

$addSubnetRequest = AddSubnetRequestBuilder::init(
    'eu-central',
    Type42Enum::SERVER
)
    ->ipRange('10.0.1.0/24')
    ->vswitchId(1000)
    ->build();
```



