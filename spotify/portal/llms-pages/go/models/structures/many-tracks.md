# Many Tracks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRk1hbnlUcmFja3M

*This model accepts additional fields of type interface{}.*


# Class Name

`ManyTracks`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tracks` | [`[]models.TrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/track-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    manyTracks := models.ManyTracks{
        Tracks:                []models.TrackObject{
            models.TrackObject{
                Album:                 models.ToPointer(models.SimplifiedAlbumObject{
                    AlbumType:             models.AlbumType_Single,
                    TotalTracks:           170,
                    AvailableMarkets:      []string{
                        "available_markets2",
                        "available_markets3",
                    },
                    ExternalUrls:          models.ExternalUrlObject{
                        Spotify:               models.ToPointer("spotify6"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    Href:                  "href0",
                    Id:                    "id8",
                    Images:                []models.ImageObject{
                        models.ImageObject{
                            Url:                   "url6",
                            Height:                models.ToPointer(182),
                            Width:                 models.ToPointer(222),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                    },
                    Name:                  "name8",
                    ReleaseDate:           "release_date6",
                    ReleaseDatePrecision:  models.ReleaseDatePrecision_Day,
                    Restrictions:          models.ToPointer(models.AlbumRestrictionObject{
                        Reason:                models.ToPointer(models.Reason_Explicit),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Type:                  "type2",
                    Uri:                   "uri2",
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
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
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
                            "genres7",
                            "genres8",
                        },
                        Href:                  models.ToPointer("href2"),
                        Id:                    models.ToPointer("id0"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
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
                            "genres7",
                            "genres8",
                        },
                        Href:                  models.ToPointer("href2"),
                        Id:                    models.ToPointer("id0"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
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
                            "genres7",
                            "genres8",
                        },
                        Href:                  models.ToPointer("href2"),
                        Id:                    models.ToPointer("id0"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                AvailableMarkets:      []string{
                    "available_markets8",
                    "available_markets9",
                },
                DiscNumber:            models.ToPointer(168),
                DurationMs:            models.ToPointer(232),
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



