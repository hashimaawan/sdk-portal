# Currently Playing Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`CurrentlyPlayingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Context` | [`*models.ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `Timestamp` | `*int64` | Optional | Unix Millisecond Timestamp when data was fetched |
| `ProgressMs` | `*int` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `IsPlaying` | `*bool` | Optional | If something is currently playing, return `true`. |
| `Item` | [`*models.CurrentlyPlayingObjectItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/oneof-anyof-definitions/currently-playing-object-item.md) | Optional | This is a container for one-of cases. |
| `CurrentlyPlayingType` | `*string` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `Actions` | [`*models.DisallowsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    currentlyPlayingObject := models.CurrentlyPlayingObject{
        Context:               models.ToPointer(models.ContextObject{
            Type:                  models.ToPointer("type8"),
            Href:                  models.ToPointer("href4"),
            ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                Spotify:               models.ToPointer("spotify6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Uri:                   models.ToPointer("uri6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Timestamp:             models.ToPointer(int64(254)),
        ProgressMs:            models.ToPointer(226),
        IsPlaying:             models.ToPointer(false),
        Item:                  models.ToPointer(models.CurrentlyPlayingObjectItemContainer.FromTrackObject(models.TrackObject{
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
            },
            AvailableMarkets:      []string{
                "available_markets6",
                "available_markets7",
            },
            DiscNumber:            models.ToPointer(30),
            DurationMs:            models.ToPointer(222),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



