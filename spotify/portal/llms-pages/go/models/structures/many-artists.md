# Many Artists

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRk1hbnlBcnRpc3Rz

*This model accepts additional fields of type interface{}.*


# Class Name

`ManyArtists`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Artists` | [`[]models.ArtistObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/artist-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    manyArtists := models.ManyArtists{
        Artists:               []models.ArtistObject{
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
                Href:                  models.ToPointer("href2"),
                Id:                    models.ToPointer("id0"),
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



