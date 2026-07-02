# V2 Images Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ImagesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Image` | [`models.Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/image-1.md) | Required | - |
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
    v2ImagesResponse2 := models.V2ImagesResponse2{
        Image:                 models.Image1{
            CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-05-04T22:23:02Z", func(err error) { log.Fatalln(err) })),
            Description:           models.ToPointer("description6"),
            Distribution:          models.ToPointer(models.Distribution_Ubuntu),
            ErrorMessage:          models.ToPointer("error_message8"),
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
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



