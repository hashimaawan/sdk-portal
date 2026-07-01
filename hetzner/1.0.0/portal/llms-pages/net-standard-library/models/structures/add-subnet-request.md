# Add Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFkZFN1Ym5ldFJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`AddSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `string` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. If the Subnet is of type vSwitch, it also can not overlap with any gateway in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. |
| `NetworkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. |
| `Type` | [`Type42`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-42.md) | Required | Type of Subnetwork |
| `VswitchId` | `int?` | Optional | ID of the robot vSwitch. Must be supplied if the subnet is of type vswitch. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

AddSubnetRequest addSubnetRequest = new AddSubnetRequest
{
    NetworkZone = "eu-central",
    Type = Type42.Server,
    IpRange = "10.0.1.0/24",
    VswitchId = 1000,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



