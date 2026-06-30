# Paging Artist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRlBhZ2luZ0FydGlzdE9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`PagingArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `Limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `*string` | Required | URL to the next page of items. ( `null` if none) |
| `Offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `Previous` | `*string` | Required | URL to the previous page of items. ( `null` if none) |
| `Total` | `int` | Required | The total number of items available to return. |
| `Items` | [`[]models.ArtistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/artist-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    pagingArtistObject := models.PagingArtistObject{
        Href:                  "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
        Limit:                 20,
        Next:                  models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
        Offset:                0,
        Previous:              models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
        Total:                 4,
        Items:                 []models.ArtistObject{
            models.ArtistObject{
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
                Href:                  models.ToPointer("href0"),
                Id:                    models.ToPointer("id8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



