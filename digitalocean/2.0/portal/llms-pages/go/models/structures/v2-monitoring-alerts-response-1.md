# V2 Monitoring Alerts Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2MonitoringAlertsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Policy` | [`*models.Policy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/policy.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2MonitoringAlertsResponse1 := models.V2MonitoringAlertsResponse1{
        Policy:                models.ToPointer(models.Policy{
            Alerts:                models.Alerts{
                Email:                 []string{
                    "email2",
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
            },
            Compare:               models.Compare_Greaterthan,
            Description:           "description4",
            Enabled:               false,
            Entities:              []string{
                "entities9",
            },
            Tags:                  []string{
                "tags9",
                "tags0",
                "tags1",
            },
            Type:                  models.Type17_EnumV1InsightsdropletdiskRead,
            Uuid:                  "uuid0",
            Value:                 float64(149.36),
            Window:                models.Window1_Enum30M,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



