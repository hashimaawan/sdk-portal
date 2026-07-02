# State 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXRlMw

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`State3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PreviousOutage` | [`*models.PreviousOutage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/previous-outage.md) | Optional | - |
| `Regions` | [`*models.Regions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/regions.md) | Optional | A map of region to regional state |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    state3 := models.State3{
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
    }

}
```



