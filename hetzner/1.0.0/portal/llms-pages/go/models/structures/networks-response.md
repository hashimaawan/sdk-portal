# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type interface{}.*


# Class Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/meta.md) | Optional | - |
| `Networks` | [`[]models.Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/network.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    networksResponse := models.NetworksResponse{
        Meta:                  models.ToPointer(models.Meta{
            Pagination:            models.Pagination{
                LastPage:              models.ToPointer(float64(77.7)),
                NextPage:              models.ToPointer(float64(209.18)),
                Page:                  float64(17.58),
                PerPage:               float64(13.34),
                PreviousPage:          models.ToPointer(float64(50.02)),
                TotalEntries:          models.ToPointer(float64(206.64)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Networks:              []models.Network{
            models.Network{
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
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



