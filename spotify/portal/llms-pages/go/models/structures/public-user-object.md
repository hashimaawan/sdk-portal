# Public User Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlB1YmxpY1VzZXJPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`PublicUserObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DisplayName` | `models.Optional[string]` | Optional | The name displayed on the user's profile. `null` if not available. |
| `ExternalUrls` | [`*models.ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. |
| `Followers` | [`*models.FollowersObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/followers-object.md) | Optional | Information about the followers of this user. |
| `Href` | `*string` | Optional | A link to the Web API endpoint for this user. |
| `Id` | `*string` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `Images` | [`[]models.ImageObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/image-object.md) | Optional | The user's profile image. |
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
    publicUserObject := models.PublicUserObject{
        DisplayName:           models.NewOptional(models.ToPointer("display_name0")),
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
        Href:                  models.ToPointer("href2"),
        Id:                    models.ToPointer("id0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



