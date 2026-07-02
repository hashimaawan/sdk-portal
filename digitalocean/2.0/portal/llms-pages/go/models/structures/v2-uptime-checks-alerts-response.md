# V2 Uptime Checks Alerts Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2UptimeChecksAlertsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Alerts` | [`[]models.Alerts1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/alerts-1.md) | Optional | - |
| `Links` | [`*models.Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links.md) | Optional | - |
| `Meta` | [`models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    v2UptimeChecksAlertsResponse := models.V2UptimeChecksAlertsResponse{
        Alerts:                []models.Alerts1{
            models.Alerts1{
                Id:                    models.ToPointer(uuid.MustParse("00000cea-0000-0000-0000-000000000000")),
                Comparison:            models.ToPointer(models.Comparison_GreaterThan),
                Name:                  models.ToPointer("name6"),
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
                Period:                models.ToPointer(models.Period_Enum10M),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Alerts1{
                Id:                    models.ToPointer(uuid.MustParse("00000cea-0000-0000-0000-000000000000")),
                Comparison:            models.ToPointer(models.Comparison_GreaterThan),
                Name:                  models.ToPointer("name6"),
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
                Period:                models.ToPointer(models.Period_Enum10M),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Alerts1{
                Id:                    models.ToPointer(uuid.MustParse("00000cea-0000-0000-0000-000000000000")),
                Comparison:            models.ToPointer(models.Comparison_GreaterThan),
                Name:                  models.ToPointer("name6"),
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
                Period:                models.ToPointer(models.Period_Enum10M),
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



