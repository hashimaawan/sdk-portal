# V2 Reserved Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ReservedIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`[]models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/action.md) | Optional | - |
| `Links` | [`*models.Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links.md) | Optional | - |
| `Meta` | [`models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    v2ReservedIpsActionsResponse := models.V2ReservedIpsActionsResponse{
        Actions:               []models.Action{
            models.Action{
                CompletedAt:           models.NewOptional(models.ToPointer(parseTime(time.RFC3339, "2015-11-21T21:51:09Z", func(err error) { log.Fatalln(err) }))),
                Id:                    models.ToPointer(72531856),
                Region:                models.ToPointer(models.Region{
                    Available:             true,
                    Features:              []string{
                        "private_networking",
                        "backups",
                        "ipv6",
                        "metadata",
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
                        "s-32vcpu-192gb",
                    },
                    Slug:                  "nyc3",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                RegionSlug:            models.NewOptional(models.ToPointer("nyc3")),
                ResourceId:            models.NewOptional(models.ToPointer(758604197)),
                ResourceType:          models.ToPointer("reserved_ip"),
                StartedAt:             models.ToPointer(parseTime(time.RFC3339, "2015-11-21T21:51:09Z", func(err error) { log.Fatalln(err) })),
                Status:                models.ToPointer(models.Status1_Completed),
                Type:                  models.ToPointer("reserve_ip"),
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



