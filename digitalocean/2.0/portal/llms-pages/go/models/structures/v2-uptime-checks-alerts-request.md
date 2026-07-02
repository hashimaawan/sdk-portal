# V2 Uptime Checks Alerts Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2UptimeChecksAlertsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Comparison` | [`*models.Comparison`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/comparison.md) | Optional | The comparison operator used against the alert's threshold. |
| `Name` | `*string` | Optional | A human-friendly display name. |
| `Notifications` | [`*models.Notifications`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/notifications.md) | Optional | The notification settings for a trigger alert. |
| `Period` | [`*models.Period`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/period.md) | Optional | Period of time the threshold must be exceeded to trigger the alert. |
| `Threshold` | `*int` | Optional | The threshold at which the alert will enter a trigger state. The specific threshold is dependent on the alert type. |
| `Type` | [`*models.Type20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-20.md) | Optional | The type of alert. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2UptimeChecksAlertsRequest := models.V2UptimeChecksAlertsRequest{
        Comparison:            models.ToPointer(models.Comparison_GreaterThan),
        Name:                  models.ToPointer("Landing page degraded performance"),
        Notifications:         models.ToPointer(models.Notifications{
            Email:                 []string{
                "email4",
                "email3",
            },
            Slack:                 []models.Slack{
                models.Slack{
                    Channel:               "channel6",
                    Url:                   "url2",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Slack{
                    Channel:               "channel6",
                    Url:                   "url2",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Slack{
                    Channel:               "channel6",
                    Url:                   "url2",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Period:                models.ToPointer(models.Period_Enum2M),
        Threshold:             models.ToPointer(300),
        Type:                  models.ToPointer(models.Type20_Latency),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



