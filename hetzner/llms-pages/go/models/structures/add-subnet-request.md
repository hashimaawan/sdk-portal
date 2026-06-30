# Add Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkFkZFN1Ym5ldFJlcXVlc3Q


# Class Name

`AddSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `*string` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. If the Subnet is of type vSwitch, it also can not overlap with any gateway in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. |
| `NetworkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. |
| `Type` | [`models.Type42Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-42.md) | Required | Type of Subnetwork |
| `VswitchId` | `*int` | Optional | ID of the robot vSwitch. Must be supplied if the subnet is of type vswitch. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    addSubnetRequest := models.AddSubnetRequest{
        IpRange:              models.ToPointer("10.0.1.0/24"),
        NetworkZone:          "eu-central",
        Type:                 models.Type42Enum_SERVER,
        VswitchId:            models.ToPointer(1000),
    }

}
```



