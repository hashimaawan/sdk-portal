# Many Albums

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRk1hbnlBbGJ1bXM

*This model accepts additional fields of type interface{}.*


# Class Name

`ManyAlbums`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Albums` | [`[]models.AlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/album-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    manyAlbums := models.ManyAlbums{
        Albums:                []models.AlbumObject{
            models.AlbumObject{
                AlbumType:             models.AlbumType_Compilation,
                TotalTracks:           9,
                AvailableMarkets:      []string{
                    "CA",
                    "BR",
                    "IT",
                },
                ExternalUrls:          models.ExternalUrlObject{
                    Spotify:               models.ToPointer("spotify6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Href:                  "href0",
                Id:                    "2up3OPMp9Tb4dAKM2erWXQ",
                Images:                []models.ImageObject{
                    models.ImageObject{
                        Url:                   "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                        Height:                models.ToPointer(300),
                        Width:                 models.ToPointer(300),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Name:                  "name8",
                ReleaseDate:           "1981-12",
                ReleaseDatePrecision:  models.ReleaseDatePrecision_Year,
                Restrictions:          models.ToPointer(models.AlbumRestrictionObject{
                    Reason:                models.ToPointer(models.Reason_Explicit),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Type:                  "album",
                Uri:                   "spotify:album:2up3OPMp9Tb4dAKM2erWXQ",
                Artists:               []models.SimplifiedArtistObject{
                    models.SimplifiedArtistObject{
                        ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                            Spotify:               models.ToPointer("spotify6"),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        Href:                  models.ToPointer("href2"),
                        Id:                    models.ToPointer("id0"),
                        Name:                  models.ToPointer("name0"),
                        Type:                  models.ToPointer(models.Type_Artist),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Tracks:                models.PagingSimplifiedTrackObject{
                    Href:                  "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
                    Limit:                 20,
                    Next:                  models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
                    Offset:                0,
                    Previous:              models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
                    Total:                 4,
                    Items:                 []models.SimplifiedTrackObject{
                        models.SimplifiedTrackObject{
                            Artists:               []models.SimplifiedArtistObject{
                                models.SimplifiedArtistObject{
                                    ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                                        Spotify:               models.ToPointer("spotify6"),
                                        AdditionalProperties:  map[string]interface{}{
                                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                        },
                                    }),
                                    Href:                  models.ToPointer("href2"),
                                    Id:                    models.ToPointer("id0"),
                                    Name:                  models.ToPointer("name0"),
                                    Type:                  models.ToPointer(models.Type_Artist),
                                    AdditionalProperties:  map[string]interface{}{
                                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                    },
                                },
                            },
                            AvailableMarkets:      []string{
                                "available_markets2",
                            },
                            DiscNumber:            models.ToPointer(244),
                            DurationMs:            models.ToPointer(52),
                            Explicit:              models.ToPointer(false),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                    },
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Copyrights:            []models.CopyrightObject{
                    models.CopyrightObject{
                        Text:                  models.ToPointer("text2"),
                        Type:                  models.ToPointer("type2"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                ExternalIds:           models.ExternalIdObject{
                    Isrc:                  models.ToPointer("isrc8"),
                    Ean:                   models.ToPointer("ean8"),
                    Upc:                   models.ToPointer("upc2"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Genres:                []string{
                    "Egg punk",
                    "Noise rock",
                },
                Label:                 "label8",
                Popularity:            66,
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



