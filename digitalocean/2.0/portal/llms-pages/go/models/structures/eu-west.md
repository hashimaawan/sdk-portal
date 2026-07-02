# Eu West

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkV1V2VzdA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`EuWest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Status` | [`*models.Status16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-16.md) | Optional | - |
| `StatusChangedAt` | `*string` | Optional | - |
| `ThirtyDayUptimePercentage` | `*float64` | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    euWest := models.EuWest{
        Status:                    models.ToPointer(models.Status16_Up),
        StatusChangedAt:           models.ToPointer("2022-03-17T22:28:51Z"),
        ThirtyDayUptimePercentage: models.ToPointer(float64(97.99)),
        AdditionalProperties:      map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



