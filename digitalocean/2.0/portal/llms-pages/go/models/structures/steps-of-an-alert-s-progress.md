# Steps of an Alert S Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlN0ZXBzJTI1MjBvZiUyNTIwYW4lMjUyMGFsZXJ0JTI1MjdzJTI1MjBwcm9ncmVzcy4

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`StepsOfAnAlertSProgress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EndedAt` | `*time.Time` | Optional | - |
| `Name` | `*string` | Optional | - |
| `Reason` | [`*models.Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/reason.md) | Optional | - |
| `StartedAt` | `*time.Time` | Optional | - |
| `Status` | [`*models.Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-2.md) | Optional | **Default**: `"UNKNOWN"` |
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
    stepsOfAnAlertSProgress := models.StepsOfAnAlertSProgress{
        EndedAt:               models.ToPointer(parseTime(time.RFC3339, "2020-11-19T20:27:18Z", func(err error) { log.Fatalln(err) })),
        Name:                  models.ToPointer("example_step"),
        Reason:                models.ToPointer(models.Reason{
            Code:                  models.ToPointer("code2"),
            Message:               models.ToPointer("message4"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        StartedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-11-19T20:27:18Z", func(err error) { log.Fatalln(err) })),
        Status:                models.ToPointer(models.Status2_Success),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



