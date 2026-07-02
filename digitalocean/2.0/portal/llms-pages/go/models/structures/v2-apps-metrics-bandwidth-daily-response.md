# V2 Apps Metrics Bandwidth Daily Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsMetricsBandwidthDailyResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AppBandwidthUsage` | [`[]models.AppBandwidthUsage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/app-bandwidth-usage.md) | Optional | A list of bandwidth usage details by app. |
| `Date` | `*time.Time` | Optional | The date for the metrics data. |
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
    v2AppsMetricsBandwidthDailyResponse := models.V2AppsMetricsBandwidthDailyResponse{
        AppBandwidthUsage:     []models.AppBandwidthUsage{
            models.AppBandwidthUsage{
                AppId:                 models.ToPointer("app_id4"),
                BandwidthBytes:        models.ToPointer("bandwidth_bytes6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.AppBandwidthUsage{
                AppId:                 models.ToPointer("app_id4"),
                BandwidthBytes:        models.ToPointer("bandwidth_bytes6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Date:                  models.ToPointer(parseTime(time.RFC3339, "2023-01-17T00:00:00Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



