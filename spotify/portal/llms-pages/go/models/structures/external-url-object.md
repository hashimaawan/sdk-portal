# External Url Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRkV4dGVybmFsVXJsT2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`ExternalUrlObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Spotify` | `*string` | Optional | The [Spotify URL](/documentation/web-api/concepts/spotify-uris-ids) for the object. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    externalUrlObject := models.ExternalUrlObject{
        Spotify:               models.ToPointer("spotify0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



