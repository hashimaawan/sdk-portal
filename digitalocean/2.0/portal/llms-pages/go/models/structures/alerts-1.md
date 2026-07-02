# Alerts 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkFsZXJ0czE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Alerts1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `*uuid.UUID` | Optional, Read-only | A unique ID that can be used to identify and reference the alert. |
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
    "github.com/google/uuid"
)

func main() {
    alerts1 := models.Alerts1{
        Id:                    models.ToPointer(uuid.MustParse("5a4981aa-9653-4bd1-bef5-d6bff52042e4")),
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



