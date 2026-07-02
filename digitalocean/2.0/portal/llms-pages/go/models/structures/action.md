# Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkFjdGlvbg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Action`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CompletedAt` | `models.Optional[time.Time]` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. |
| `Id` | `*int` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `Region` | [`*models.Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/region.md) | Optional | - |
| `RegionSlug` | `models.Optional[string]` | Optional | - |
| `ResourceId` | `models.Optional[int]` | Optional | A unique identifier for the resource that the action is associated with. |
| `ResourceType` | `*string` | Optional | The type of resource that the action is associated with. |
| `StartedAt` | `*time.Time` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. |
| `Status` | [`*models.Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `"in-progress"` |
| `Type` | `*string` | Optional | This is the type of action that the object represents. For example, this could be "transfer" to represent the state of an image transfer action. |
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
    action := models.Action{
        CompletedAt:           models.NewOptional(models.ToPointer(parseTime(time.RFC3339, "2020-11-14T16:30:06Z", func(err error) { log.Fatalln(err) }))),
        Id:                    models.ToPointer(36804636),
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
        RegionSlug:            models.NewOptional(models.ToPointer("region_slug0")),
        ResourceId:            models.NewOptional(models.ToPointer(3164444)),
        ResourceType:          models.ToPointer("droplet"),
        StartedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-11-14T16:29:21Z", func(err error) { log.Fatalln(err) })),
        Status:                models.ToPointer(models.Status1_Completed),
        Type:                  models.ToPointer("create"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



