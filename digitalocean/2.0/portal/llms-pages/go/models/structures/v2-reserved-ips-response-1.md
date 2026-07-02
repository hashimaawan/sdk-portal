# V2 Reserved Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ReservedIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Links` | [`*models.Links3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links-3.md) | Optional | - |
| `ReservedIp` | [`*models.ReservedIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/reserved-ip.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    v2ReservedIpsResponse1 := models.V2ReservedIpsResponse1{
        Links:                 models.ToPointer(models.Links3{
            Actions:               []models.Action1{
                models.Action1{
                    Href:                  models.ToPointer("href0"),
                    Id:                    models.ToPointer(154),
                    Rel:                   models.ToPointer("rel4"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Droplets:              []models.Action1{
                models.Action1{
                    Href:                  models.ToPointer("href2"),
                    Id:                    models.ToPointer(232),
                    Rel:                   models.ToPointer("rel6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Action1{
                    Href:                  models.ToPointer("href2"),
                    Id:                    models.ToPointer(232),
                    Rel:                   models.ToPointer("rel6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        ReservedIp:            models.ToPointer(models.ReservedIp{
            Droplet:               models.ToPointer(models.ReservedIpDropletContainer.FromObject(interface{}("[key1, val1][key2, val2]"))),
            Ip:                    models.ToPointer("ip6"),
            Locked:                models.ToPointer(false),
            ProjectId:             models.ToPointer(uuid.MustParse("00002548-0000-0000-0000-000000000000")),
            Region:                models.ToPointer(models.Region{
                Available:             false,
                Features:              []string{
                    "features7",
                    "features8",
                    "features9",
                },
                Name:                  "name6",
                Sizes:                 []string{
                    "sizes6",
                },
                Slug:                  "slug0",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
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



