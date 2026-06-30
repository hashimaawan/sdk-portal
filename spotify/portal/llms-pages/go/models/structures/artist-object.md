# Artist Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRkFydGlzdE9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`ArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalUrls` | [`*models.ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. |
| `Followers` | [`*models.FollowersObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/followers-object.md) | Optional | Information about the followers of the artist. |
| `Genres` | `[]string` | Optional | A list of the genres the artist is associated with. If not yet classified, the array is empty. |
| `Href` | `*string` | Optional | A link to the Web API endpoint providing full details of the artist. |
| `Id` | `*string` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `Images` | [`[]models.ImageObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/image-object.md) | Optional | Images of the artist in various sizes, widest first. |
| `Name` | `*string` | Optional | The name of the artist. |
| `Popularity` | `*int` | Optional | The popularity of the artist. The value will be between 0 and 100, with 100 being the most popular. The artist's popularity is calculated from the popularity of all the artist's tracks. |
| `Type` | [`*models.Type`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/enumerations/type.md) | Optional | The object type. |
| `Uri` | `*string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    artistObject := models.ArtistObject{
        ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
            Spotify:               models.ToPointer("spotify6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Followers:             models.ToPointer(models.FollowersObject{
            Href:                  models.NewOptional(models.ToPointer("href0")),
            Total:                 models.ToPointer(82),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Genres:                []string{
            "Prog rock",
            "Grunge",
        },
        Href:                  models.ToPointer("href8"),
        Id:                    models.ToPointer("id6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



