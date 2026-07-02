# V2 Domains Records Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DomainsRecordsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DomainRecords` | [`[]models.DomainRecord`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/domain-record.md) | Optional | - |
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
    v2DomainsRecordsResponse := models.V2DomainsRecordsResponse{
        DomainRecords:         []models.DomainRecord{
            models.DomainRecord{
                Data:                  models.ToPointer("data2"),
                Flags:                 models.NewOptional(models.ToPointer(216)),
                Id:                    models.ToPointer(172),
                Name:                  models.ToPointer("name2"),
                Port:                  models.NewOptional(models.ToPointer(92)),
                Type:                  "type8",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.DomainRecord{
                Data:                  models.ToPointer("data2"),
                Flags:                 models.NewOptional(models.ToPointer(216)),
                Id:                    models.ToPointer(172),
                Name:                  models.ToPointer("name2"),
                Port:                  models.NewOptional(models.ToPointer(92)),
                Type:                  "type8",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.DomainRecord{
                Data:                  models.ToPointer("data2"),
                Flags:                 models.NewOptional(models.ToPointer(216)),
                Id:                    models.ToPointer(172),
                Name:                  models.ToPointer("name2"),
                Port:                  models.NewOptional(models.ToPointer(92)),
                Type:                  "type8",
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



