# Playlist User Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlBsYXlsaXN0VXNlck9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`PlaylistUserObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalUrls` | [`*models.ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. |
| `Followers` | [`*models.FollowersObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/followers-object.md) | Optional | Information about the followers of this user. |
| `Href` | `*string` | Optional | A link to the Web API endpoint for this user. |
| `Id` | `*string` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `Type` | [`*models.Type3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/enumerations/type-3.md) | Optional | The object type. |
| `Uri` | `*string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    playlistUserObject := models.PlaylistUserObject{
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
        Href:                  models.ToPointer("href0"),
        Id:                    models.ToPointer("id8"),
        Type:                  models.ToPointer(models.Type3_User),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



