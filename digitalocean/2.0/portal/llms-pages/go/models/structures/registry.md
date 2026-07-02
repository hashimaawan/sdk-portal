# Registry

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlZ2lzdHJ5

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Registry`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the registry was created. |
| `Name` | `*string` | Optional | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` |
| `Region` | `*string` | Optional | Slug of the region where registry data is stored |
| `StorageUsageBytes` | `*int` | Optional, Read-only | The amount of storage used in the registry in bytes. |
| `StorageUsageBytesUpdatedAt` | `*time.Time` | Optional, Read-only | The time at which the storage usage was updated. Storage usage is calculated asynchronously, and may not immediately reflect pushes to the registry. |
| `Subscription` | [`*models.Subscription`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/subscription.md) | Optional | - |
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
    registry := models.Registry{
        CreatedAt:                  models.ToPointer(parseTime(time.RFC3339, "2020-03-21T16:02:37Z", func(err error) { log.Fatalln(err) })),
        Name:                       models.ToPointer("example"),
        Region:                     models.ToPointer("fra1"),
        StorageUsageBytes:          models.ToPointer(29393920),
        StorageUsageBytesUpdatedAt: models.ToPointer(parseTime(time.RFC3339, "2020-11-04T21:39:49.530562231Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:       map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



