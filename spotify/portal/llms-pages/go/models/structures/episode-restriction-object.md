# Episode Restriction Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkVwaXNvZGVSZXN0cmljdGlvbk9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`EpisodeRestrictionObject`


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
    episodeRestrictionObject := models.EpisodeRestrictionObject{
        Reason:                models.ToPointer("reason8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



