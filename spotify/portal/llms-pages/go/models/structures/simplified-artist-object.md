# Simplified Artist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`SimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalUrls` | [`*models.ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. |
| `Href` | `*string` | Optional | A link to the Web API endpoint providing full details of the artist. |
| `Id` | `*string` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `Name` | `*string` | Optional | The name of the artist. |
| `Type` | [`*models.Type`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/enumerations/type.md) | Optional | The object type. |
| `Uri` | `*string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    simplifiedArtistObject := models.SimplifiedArtistObject{
        ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
            Spotify:               models.ToPointer("spotify6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Href:                  models.ToPointer("href6"),
        Id:                    models.ToPointer("id4"),
        Name:                  models.ToPointer("name4"),
        Type:                  models.ToPointer(models.Type_Artist),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



