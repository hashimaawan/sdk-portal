# V2 Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2SnapshotsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Snapshots` | [`[]models.Snapshot`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/snapshot.md) | Optional | - |
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
    v2SnapshotsResponse := models.V2SnapshotsResponse{
        Snapshots:             []models.Snapshot{
            models.Snapshot{
                Id:                    "id2",
                CreatedAt:             parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) }),
                MinDiskSize:           112,
                Name:                  "name2",
                Regions:               []string{
                    "regions7",
                    "regions8",
                },
                SizeGigabytes:         float64(148.48),
                ResourceId:            "resource_id8",
                ResourceType:          models.ResourceType1_Droplet,
                Tags:                  []string{
                    "tags7",
                    "tags8",
                    "tags9",
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Snapshot{
                Id:                    "id2",
                CreatedAt:             parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) }),
                MinDiskSize:           112,
                Name:                  "name2",
                Regions:               []string{
                    "regions7",
                    "regions8",
                },
                SizeGigabytes:         float64(148.48),
                ResourceId:            "resource_id8",
                ResourceType:          models.ResourceType1_Droplet,
                Tags:                  []string{
                    "tags7",
                    "tags8",
                    "tags9",
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Snapshot{
                Id:                    "id2",
                CreatedAt:             parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) }),
                MinDiskSize:           112,
                Name:                  "name2",
                Regions:               []string{
                    "regions7",
                    "regions8",
                },
                SizeGigabytes:         float64(148.48),
                ResourceId:            "resource_id8",
                ResourceType:          models.ResourceType1_Droplet,
                Tags:                  []string{
                    "tags7",
                    "tags8",
                    "tags9",
                },
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



