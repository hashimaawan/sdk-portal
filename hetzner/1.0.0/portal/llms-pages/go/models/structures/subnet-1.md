# Subnet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlN1Ym5ldDE

*This model accepts additional fields of type interface{}.*


# Class Name

`Subnet1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `*string` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. |
| `NetworkZone` | `string` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. |
| `Type` | [`models.Type42`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-42.md) | Required | Type of Subnetwork |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    subnet1 := models.Subnet1{
        IpRange:               models.ToPointer("10.0.1.0/24"),
        NetworkZone:           "eu-central",
        Type:                  models.Type42_Vswitch,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



