# Device Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkRldmljZU9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`DeviceObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `models.Optional[string]` | Optional | The device ID. This ID is unique and persistent to some extent. However, this is not guaranteed and any cached `device_id` should periodically be cleared out and refetched as necessary. |
| `IsActive` | `*bool` | Optional | If this device is the currently active device. |
| `IsPrivateSession` | `*bool` | Optional | If this device is currently in a private session. |
| `IsRestricted` | `*bool` | Optional | Whether controlling this device is restricted. At present if this is "true" then no Web API commands will be accepted by this device. |
| `Name` | `*string` | Optional | A human-readable name for the device. Some devices have a name that the user can configure (e.g. \"Loudest speaker\") and some devices have a generic name associated with the manufacturer or device model. |
| `Type` | `*string` | Optional | Device type, such as "computer", "smartphone" or "speaker". |
| `VolumePercent` | `models.Optional[int]` | Optional | The current volume in percent.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `SupportsVolume` | `*bool` | Optional | If this device can be used to set the volume. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    deviceObject := models.DeviceObject{
        Id:                    models.NewOptional(models.ToPointer("id0")),
        IsActive:              models.ToPointer(false),
        IsPrivateSession:      models.ToPointer(false),
        IsRestricted:          models.ToPointer(false),
        Name:                  models.ToPointer("Kitchen speaker"),
        Type:                  models.ToPointer("computer"),
        VolumePercent:         models.NewOptional(models.ToPointer(59)),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



