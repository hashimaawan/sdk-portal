# Explicit Content Settings Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkV4cGxpY2l0Q29udGVudFNldHRpbmdzT2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`ExplicitContentSettingsObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FilterEnabled` | `*bool` | Optional | When `true`, indicates that explicit content should not be played. |
| `FilterLocked` | `*bool` | Optional | When `true`, indicates that the explicit content setting is locked and can't be changed by the user. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    explicitContentSettingsObject := models.ExplicitContentSettingsObject{
        FilterEnabled:         models.ToPointer(false),
        FilterLocked:          models.ToPointer(false),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



