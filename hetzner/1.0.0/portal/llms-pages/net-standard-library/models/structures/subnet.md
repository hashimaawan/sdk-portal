# Subnet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN1Ym5ldA


# Class Name

`Subnet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Gateway` | `string` | Required | Gateway for Servers attached to this subnet. For subnets of type Server this is always the first IP of the network IP range. |
| `IpRange` | `string` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. |
| `NetworkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. |
| `Type` | [`Type42Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-42.md) | Required | Type of Subnetwork |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Subnet subnet = new Subnet
{
    Gateway = "10.0.0.1",
    NetworkZone = "eu-central",
    Type = Type42Enum.Server,
    IpRange = "10.0.1.0/24",
};
```



