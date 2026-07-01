# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Network` | [`*models.Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/network.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    networksResponse1 := models.NetworksResponse1{
        Network:              models.ToPointer(models.Network{
            Created:              "created4",
            Id:                   78,
            IpRange:              "ip_range6",
            Labels:               interface{}("[key1, val1][key2, val2]"),
            LoadBalancers:        []int{
                208,
            },
            Name:                 "name4",
            Protection:           models.Protection11{
                Delete:               false,
            },
            Routes:               []models.Route{
                models.Route{
                    Destination:          "destination8",
                    Gateway:              "gateway6",
                },
                models.Route{
                    Destination:          "destination8",
                    Gateway:              "gateway6",
                },
                models.Route{
                    Destination:          "destination8",
                    Gateway:              "gateway6",
                },
            },
            Servers:              []int{
                93,
            },
            Subnets:              []models.Subnet{
                models.Subnet{
                    Gateway:              "gateway4",
                    IpRange:              models.ToPointer("ip_range6"),
                    NetworkZone:          "network_zone2",
                    Type:                 models.Type42Enum_CLOUD,
                },
            },
        }),
    }

}
```



