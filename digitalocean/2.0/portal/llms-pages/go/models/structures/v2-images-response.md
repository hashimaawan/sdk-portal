# V2 Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Images` | [`[]models.Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/image-1.md) | Required | - |
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
    v2ImagesResponse := models.V2ImagesResponse{
        Images:                []models.Image1{
            models.Image1{
                CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-05-04T22:23:02Z", func(err error) { log.Fatalln(err) })),
                Description:           models.ToPointer("description2"),
                Distribution:          models.ToPointer(models.Distribution_Ubuntu),
                ErrorMessage:          models.ToPointer("error_message4"),
                Id:                    models.ToPointer(7555620),
                MinDiskSize:           models.NewOptional(models.ToPointer(20)),
                Name:                  models.ToPointer("Nifty New Snapshot"),
                Public:                models.ToPointer(true),
                Regions:               []models.Region2{
                    models.Region2_Nyc1,
                    models.Region2_Nyc2,
                },
                SizeGigabytes:         models.NewOptional(models.ToPointer(float64(2.34))),
                Slug:                  models.NewOptional(models.ToPointer("nifty1")),
                Status:                models.ToPointer(models.Status7_New),
                Tags:                  models.NewOptional(models.ToPointer([]string{
                    "base-image",
                    "prod",
                })),
                Type:                  models.ToPointer(models.Type9_Snapshot),
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



