# Subnet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlN1Ym5ldDE


# Class Name

`Subnet1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipRange` | `?string` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. | getIpRange(): ?string | setIpRange(?string ipRange): void |
| `networkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. | getNetworkZone(): string | setNetworkZone(string networkZone): void |
| `type` | [`string(Type42Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-42.md) | Required | Type of Subnetwork | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Subnet1Builder;
use HetznerCloudAPILib\Models\Type42Enum;

$subnet1 = Subnet1Builder::init(
    'eu-central',
    Type42Enum::VSWITCH
)
    ->ipRange('10.0.1.0/24')
    ->build();
```



