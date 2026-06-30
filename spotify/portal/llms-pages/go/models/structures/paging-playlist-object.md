# Paging Playlist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlBhZ2luZ1BsYXlsaXN0T2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`PagingPlaylistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `Limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `*string` | Required | URL to the next page of items. ( `null` if none) |
| `Offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `Previous` | `*string` | Required | URL to the previous page of items. ( `null` if none) |
| `Total` | `int` | Required | The total number of items available to return. |
| `Items` | [`[]models.SimplifiedPlaylistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/simplified-playlist-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    pagingPlaylistObject := models.PagingPlaylistObject{
        Href:                  "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
        Limit:                 20,
        Next:                  models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
        Offset:                0,
        Previous:              models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
        Total:                 4,
        Items:                 []models.SimplifiedPlaylistObject{
            models.SimplifiedPlaylistObject{
                Collaborative:         models.ToPointer(false),
                Description:           models.ToPointer("description2"),
                ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                    Spotify:               models.ToPointer("spotify6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
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



