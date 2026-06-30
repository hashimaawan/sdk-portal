# Many Devices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRk1hbnlEZXZpY2Vz

*This model accepts additional fields of type interface{}.*


# Class Name

`ManyDevices`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Devices` | [`[]models.DeviceObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/device-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    manyDevices := models.ManyDevices{
        Devices:               []models.DeviceObject{
            models.DeviceObject{
                Id:                    models.NewOptional(models.ToPointer("id4")),
                IsActive:              models.ToPointer(false),
                IsPrivateSession:      models.ToPointer(false),
                IsRestricted:          models.ToPointer(false),
                Name:                  models.ToPointer("Kitchen speaker"),
                Type:                  models.ToPointer("computer"),
                VolumePercent:         models.NewOptional(models.ToPointer(59)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



