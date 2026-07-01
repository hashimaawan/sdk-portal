# Create Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`CreateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `string` | Required | IP range of the whole network which must span all included subnets. Must be one of the private IPv4 ranges of RFC1918. Minimum network size is /24. We highly recommend that you pick a larger network with a /16 netmask. |
| `Labels` | [`*models.Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the network |
| `Routes` | [`[]models.Route`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/route.md) | Optional | Array of routes set in this network. The destination of the route must be one of the private IPv4 ranges of RFC1918. The gateway must be a subnet/IP of the ip_range of the network object. The destination must not overlap with an existing ip_range in any subnets or with any destinations in other routes or with the first IP of the networks ip_range or with 172.31.1.1. The gateway cannot be the first IP of the networks ip_range and also cannot be 172.31.1.1. |
| `Subnets` | [`[]models.Subnet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/subnet-1.md) | Optional | Array of subnets allocated. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createNetworkRequest := models.CreateNetworkRequest{
        IpRange:              "10.0.0.0/16",
        Labels:               models.ToPointer(models.Labels{
            Labelkey:             models.ToPointer("labelkey4"),
        }),
        Name:                 "mynet",
        Routes:               []models.Route{
            models.Route{
                Destination:          "destination8",
                Gateway:              "gateway6",
            },
        },
        Subnets:              []models.Subnet1{
            models.Subnet1{
                IpRange:              models.ToPointer("ip_range6"),
                NetworkZone:          "network_zone2",
                Type:                 models.Type42Enum_CLOUD,
            },
            models.Subnet1{
                IpRange:              models.ToPointer("ip_range6"),
                NetworkZone:          "network_zone2",
                Type:                 models.Type42Enum_CLOUD,
            },
            models.Subnet1{
                IpRange:              models.ToPointer("ip_range6"),
                NetworkZone:          "network_zone2",
                Type:                 models.Type42Enum_CLOUD,
            },
        },
    }

}
```



