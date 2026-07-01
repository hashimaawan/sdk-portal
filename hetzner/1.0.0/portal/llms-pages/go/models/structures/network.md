# Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRk5ldHdvcms

*This model accepts additional fields of type interface{}.*


# Class Name

`Network`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Created` | `string` | Required | Point in time when the Network was created (in ISO-8601 format) |
| `Id` | `int` | Required | ID of the Network |
| `IpRange` | `string` | Required | IPv4 prefix of the whole Network |
| `Labels` | `interface{}` | Required | User-defined labels (key-value pairs) |
| `LoadBalancers` | `[]int` | Optional | Array of IDs of Load Balancers attached to this Network |
| `Name` | `string` | Required | Name of the Network |
| `Protection` | [`models.Protection11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/protection-11.md) | Required | Protection configuration for the Network |
| `Routes` | [`[]models.Route`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/route.md) | Required | Array of routes set in this Network |
| `Servers` | `[]int` | Required | Array of IDs of Servers attached to this Network |
| `Subnets` | [`[]models.Subnet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/subnet.md) | Required | Array subnets allocated in this Network |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    network := models.Network{
        Created:               "2016-01-30T23:50:00+00:00",
        Id:                    4711,
        IpRange:               "10.0.0.0/16",
        Labels:                interface{}("[key1, val1][key2, val2]"),
        LoadBalancers:         []int{
            42,
        },
        Name:                  "mynet",
        Protection:            models.Protection11{
            Delete:                false,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        Routes:                []models.Route{
            models.Route{
                Destination:           "10.100.1.0/24",
                Gateway:               "10.0.1.1",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Servers:               []int{
            42,
        },
        Subnets:               []models.Subnet{
            models.Subnet{
                Gateway:               "10.0.0.1",
                IpRange:               models.ToPointer("10.0.1.0/24"),
                NetworkZone:           "eu-central",
                Type:                  models.Type42_Cloud,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



