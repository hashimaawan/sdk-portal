# V2 Droplets Backups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQmFja3VwcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DropletsBackupsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Backups` | [`[]models.Backup1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/backup-1.md) | Optional | - |
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
    v2DropletsBackupsResponse := models.V2DropletsBackupsResponse{
        Backups:               []models.Backup1{
            models.Backup1{
                Id:                    196,
                CreatedAt:             parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) }),
                MinDiskSize:           242,
                Name:                  "name4",
                Regions:               []string{
                    "regions9",
                    "regions0",
                    "regions1",
                },
                SizeGigabytes:         float64(180.5),
                Type:                  models.Type13_Snapshot,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Backup1{
                Id:                    196,
                CreatedAt:             parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) }),
                MinDiskSize:           242,
                Name:                  "name4",
                Regions:               []string{
                    "regions9",
                    "regions0",
                    "regions1",
                },
                SizeGigabytes:         float64(180.5),
                Type:                  models.Type13_Snapshot,
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



