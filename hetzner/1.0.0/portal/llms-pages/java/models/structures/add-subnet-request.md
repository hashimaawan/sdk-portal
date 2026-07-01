# Add Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFkZFN1Ym5ldFJlcXVlc3Q


# Class Name

`AddSubnetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IpRange` | `String` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. If the Subnet is of type vSwitch, it also can not overlap with any gateway in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. | String getIpRange() | setIpRange(String ipRange) |
| `NetworkZone` | `String` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. | String getNetworkZone() | setNetworkZone(String networkZone) |
| `Type` | [`Type42Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-42.md) | Required | Type of Subnetwork | Type42Enum getType() | setType(Type42Enum type) |
| `VswitchId` | `Integer` | Optional | ID of the robot vSwitch. Must be supplied if the subnet is of type vswitch. | Integer getVswitchId() | setVswitchId(Integer vswitchId) |


# Example

```java
import cloud.hetzner.api.models.AddSubnetRequest;
import cloud.hetzner.api.models.Type42Enum;

AddSubnetRequest addSubnetRequest = new AddSubnetRequest.Builder(
    "eu-central",
    Type42Enum.SERVER
)
.ipRange("10.0.1.0/24")
.vswitchId(1000)
.build();
```



