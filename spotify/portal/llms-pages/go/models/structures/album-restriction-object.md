# Album Restriction Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkFsYnVtUmVzdHJpY3Rpb25PYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`AlbumRestrictionObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Reason` | [`*models.Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/enumerations/reason.md) | Optional | The reason for the restriction. Albums may be restricted if the content is not available in a given market, to the user's subscription type, or when the user's account is set to not play explicit content.<br>Additional reasons may be added in the future. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    albumRestrictionObject := models.AlbumRestrictionObject{
        Reason:                models.ToPointer(models.Reason_Market),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



