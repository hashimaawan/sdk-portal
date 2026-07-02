# V2 Floating Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBGbG9hdGluZyUyNTIwSXBzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2FloatingIpsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FloatingIps` | [`[]models.FloatingIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/floating-ip-1.md) | Optional | - |
| `Links` | [`*models.Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links.md) | Optional | - |
| `Meta` | [`models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    v2FloatingIpsResponse := models.V2FloatingIpsResponse{
        FloatingIps:           []models.FloatingIp1{
            models.FloatingIp1{
                Droplet:               nil,
                Ip:                    models.ToPointer("45.55.96.47"),
                Locked:                models.ToPointer(false),
                ProjectId:             models.ToPointer(uuid.MustParse("746c6152-2fa2-11ed-92d3-27aaa54e4988")),
                Region:                models.ToPointer(models.Region{
                    Available:             true,
                    Features:              []string{
                        "private_networking",
                        "backups",
                        "ipv6",
                        "metadata",
                        "install_agent",
                        "storage",
                        "image_transfer",
                    },
                    Name:                  "New York 3",
                    Sizes:                 []string{
                        "s-1vcpu-1gb",
                        "s-1vcpu-2gb",
                        "s-1vcpu-3gb",
                        "s-2vcpu-2gb",
                        "s-3vcpu-1gb",
                        "s-2vcpu-4gb",
                        "s-4vcpu-8gb",
                        "s-6vcpu-16gb",
                        "s-8vcpu-32gb",
                        "s-12vcpu-48gb",
                        "s-16vcpu-64gb",
                        "s-20vcpu-96gb",
                        "s-24vcpu-128gb",
                        "s-32vcpu-192g",
                    },
                    Slug:                  "nyc3",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
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
            Total:                 1,
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



