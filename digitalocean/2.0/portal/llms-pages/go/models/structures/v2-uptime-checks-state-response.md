# V2 Uptime Checks State Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwU3RhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2UptimeChecksStateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `State` | [`*models.State3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/state-3.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2UptimeChecksStateResponse := models.V2UptimeChecksStateResponse{
        State:                 models.ToPointer(models.State3{
            PreviousOutage:        models.ToPointer(models.PreviousOutage{
                DurationSeconds:       models.ToPointer(16),
                EndedAt:               models.ToPointer("ended_at4"),
                Region:                models.ToPointer("region8"),
                StartedAt:             models.ToPointer("started_at4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Regions:               models.ToPointer(models.Regions{
                EuWest:                models.ToPointer(models.EuWest{
                    Status:                    models.ToPointer(models.Status16_Down),
                    StatusChangedAt:           models.ToPointer("status_changed_at4"),
                    ThirtyDayUptimePercentage: models.ToPointer(float64(227.78)),
                    AdditionalProperties:      map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                UsEast:                models.ToPointer(models.EuWest{
                    Status:                    models.ToPointer(models.Status16_Down),
                    StatusChangedAt:           models.ToPointer("status_changed_at4"),
                    ThirtyDayUptimePercentage: models.ToPointer(float64(121.56)),
                    AdditionalProperties:      map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
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



