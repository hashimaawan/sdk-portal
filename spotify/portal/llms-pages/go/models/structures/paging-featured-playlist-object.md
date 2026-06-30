# Paging Featured Playlist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRlBhZ2luZ0ZlYXR1cmVkUGxheWxpc3RPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`PagingFeaturedPlaylistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Message` | `*string` | Optional | The localized message of a playlist. |
| `Playlists` | [`*models.PagingPlaylistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/paging-playlist-object.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    pagingFeaturedPlaylistObject := models.PagingFeaturedPlaylistObject{
        Message:               models.ToPointer("Popular Playlists"),
        Playlists:             models.ToPointer(models.PagingPlaylistObject{
            Href:                  "href2",
            Limit:                 68,
            Next:                  models.ToPointer("next2"),
            Offset:                164,
            Previous:              models.ToPointer("previous8"),
            Total:                 162,
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
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



