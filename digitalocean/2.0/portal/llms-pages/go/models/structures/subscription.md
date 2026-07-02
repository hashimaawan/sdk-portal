# Subscription

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvbg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Subscription`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*time.Time` | Optional, Read-only | The time at which the subscription was created. |
| `Tier` | [`*models.Tier1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/tier-1.md) | Optional | - |
| `UpdatedAt` | `*time.Time` | Optional, Read-only | The time at which the subscription was last updated. |
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
    subscription := models.Subscription{
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-01-23T21:19:12Z", func(err error) { log.Fatalln(err) })),
        Tier:                  models.ToPointer(models.Tier1{
            AllowStorageOverage:        models.ToPointer(false),
            IncludedBandwidthBytes:     models.ToPointer(int64(46)),
            IncludedRepositories:       models.ToPointer(68),
            IncludedStorageBytes:       models.ToPointer(int64(112)),
            MonthlyPriceInCents:        models.ToPointer(110),
            AdditionalProperties:       map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-11-05T15:53:24Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



