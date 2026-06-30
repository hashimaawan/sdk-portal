# Track Restriction Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlRyYWNrUmVzdHJpY3Rpb25PYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`TrackRestrictionObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Reason` | `*string` | Optional | The reason for the restriction. Supported values:<br><br>- `market` - The content item is not available in the given market.<br>- `product` - The content item is not available for the user's subscription type.<br>- `explicit` - The content item is explicit and the user's account is set to not play explicit content.<br><br>Additional reasons may be added in the future.<br>**Note**: If you use this field, make sure that your application safely handles unknown values. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    trackRestrictionObject := models.TrackRestrictionObject{
        Reason:                models.ToPointer("reason6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



