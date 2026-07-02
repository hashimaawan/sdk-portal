# Regions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlZ2lvbnM

A map of region to regional state

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Regions`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EuWest` | [`*models.EuWest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/eu-west.md) | Optional | - |
| `UsEast` | [`*models.EuWest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/eu-west.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    regions := models.Regions{
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
    }

}
```



