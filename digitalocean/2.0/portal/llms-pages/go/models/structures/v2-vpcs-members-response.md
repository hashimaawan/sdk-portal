# V2 Vpcs Members Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBWcGNzJTI1MjBNZW1iZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2VpcsMembersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Members` | [`[]models.Member`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/member.md) | Optional | - |
| `Links` | [`*models.Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links.md) | Optional | - |
| `Meta` | [`models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2VpcsMembersResponse := models.V2VpcsMembersResponse{
        Members:               []models.Member{
            models.Member{
                CreatedAt:             models.ToPointer("2020-03-13T19:30:48Z"),
                Name:                  models.ToPointer("nyc1-load-balancer-01"),
                Urn:                   models.ToPointer("do:loadbalancer:fb294d78-d193-4cb2-8737-ea620993591b"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Member{
                CreatedAt:             models.ToPointer("2020-03-13T19:30:18Z"),
                Name:                  models.ToPointer("db-postgresql-nyc1-55986"),
                Urn:                   models.ToPointer("do:dbaas:13f7a2f6-43df-4c4a-8129-8733267ddeea"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Member{
                CreatedAt:             models.ToPointer("2020-03-13T19:30:16Z"),
                Name:                  models.ToPointer("k8s-nyc1-1584127772221"),
                Urn:                   models.ToPointer("do:kubernetes:da39d893-96e1-4e4d-971d-1fdda33a46b1"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Member{
                CreatedAt:             models.ToPointer("2020-03-13T19:29:20Z"),
                Name:                  models.ToPointer("ubuntu-s-1vcpu-1gb-nyc1-01"),
                Urn:                   models.ToPointer("do:droplet:86e29982-03a7-4946-8a07-a0114dff8754"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Links:                 models.ToPointer(models.Links{
            Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
                Last:                  models.ToPointer("last6"),
                Next:                  models.ToPointer("next2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Meta:                  models.Meta{
            Total:                 4,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



