# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ


# Class Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/meta.md) | Optional | - |
| `Networks` | [`[]models.Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/network.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    networksResponse := models.NetworksResponse{
        Meta:                 models.ToPointer(models.Meta{
            Pagination:           models.Pagination{
                LastPage:             models.ToPointer(float64(77.7)),
                NextPage:             models.ToPointer(float64(209.18)),
                Page:                 float64(17.58),
                PerPage:              float64(13.34),
                PreviousPage:         models.ToPointer(float64(50.02)),
                TotalEntries:         models.ToPointer(float64(206.64)),
            },
        }),
        Networks:             []models.Network{
            models.Network{
                Created:              "2016-01-30T23:50:00+00:00",
                Id:                   4711,
                IpRange:              "10.0.0.0/16",
                Labels:               interface{}("[key1, val1][key2, val2]"),
                LoadBalancers:        []int{
                    42,
                },
                Name:                 "mynet",
                Protection:           models.Protection11{
                    Delete:               false,
                },
                Routes:               []models.Route{
                    models.Route{
                        Destination:          "10.100.1.0/24",
                        Gateway:              "10.0.1.1",
                    },
                },
                Servers:              []int{
                    42,
                },
                Subnets:              []models.Subnet{
                    models.Subnet{
                        Gateway:              "10.0.0.1",
                        IpRange:              models.ToPointer("10.0.1.0/24"),
                        NetworkZone:          "eu-central",
                        Type:                 models.Type42Enum_CLOUD,
                    },
                },
            },
        },
    }

}
```



