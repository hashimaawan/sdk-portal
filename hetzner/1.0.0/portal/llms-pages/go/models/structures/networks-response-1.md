# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type interface{}.*


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Network` | [`*models.Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/network.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    networksResponse1 := models.NetworksResponse1{
        Network:               models.ToPointer(models.Network{
            Created:               "created4",
            Id:                    78,
            IpRange:               "ip_range6",
            Labels:                interface{}("[key1, val1][key2, val2]"),
            LoadBalancers:         []int{
                208,
            },
            Name:                  "name4",
            Protection:            models.Protection11{
                Delete:                false,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            Routes:                []models.Route{
                models.Route{
                    Destination:           "destination8",
                    Gateway:               "gateway6",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Route{
                    Destination:           "destination8",
                    Gateway:               "gateway6",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Route{
                    Destination:           "destination8",
                    Gateway:               "gateway6",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Servers:               []int{
                93,
            },
            Subnets:               []models.Subnet{
                models.Subnet{
                    Gateway:               "gateway4",
                    IpRange:               models.ToPointer("ip_range6"),
                    NetworkZone:           "network_zone2",
                    Type:                  models.Type42_Cloud,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



