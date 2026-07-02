# V2 Projects Default Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResourcesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Resources` | [`[]models.Resources1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/resources-1.md) | Optional | - |
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
    v2ProjectsDefaultResourcesResponse := models.V2ProjectsDefaultResourcesResponse{
        Resources:             []models.Resources1{
            models.Resources1{
                AssignedAt:            models.ToPointer(parseTime(time.RFC3339, "2018-09-28T19:26:37Z", func(err error) { log.Fatalln(err) })),
                Links:                 models.ToPointer(models.Links4{
                    Self:                  models.ToPointer("https://api.digitalocean.com/v2/droplets/13457723"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Status:                models.ToPointer(models.Status14_Ok),
                Urn:                   models.ToPointer("do:droplet:13457723"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Resources1{
                AssignedAt:            models.ToPointer(parseTime(time.RFC3339, "2019-03-31T16:24:14Z", func(err error) { log.Fatalln(err) })),
                Links:                 models.ToPointer(models.Links4{
                    Self:                  models.ToPointer("https://api.digitalocean.com/v2/domains/example.com"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Status:                models.ToPointer(models.Status14_Ok),
                Urn:                   models.ToPointer("do:domain:example.com"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Links:                 models.ToPointer(models.Links{
            Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
                Last:                  models.ToPointer("https://api.digitalocean.com/v2/projects/4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679/resources?page=1"),
                Next:                  models.ToPointer("next2"),
                AdditionalProperties:  map[string]interface{}{
                    "first": interface{}("https://api.digitalocean.com/v2/projects/4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679/resources?page=1"),
                },
            })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Meta:                  models.Meta{
            Total:                 2,
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



