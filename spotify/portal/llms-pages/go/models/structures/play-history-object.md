# Play History Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlBsYXlIaXN0b3J5T2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`PlayHistoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Track` | [`*models.TrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/track-object.md) | Optional | The track the user listened to. |
| `PlayedAt` | `*time.Time` | Optional | The date and time the track was played. |
| `Context` | [`*models.ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/context-object.md) | Optional | The context the track was played from. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    playHistoryObject := models.PlayHistoryObject{
        Track:                 models.ToPointer(models.TrackObject{
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
            },
            AvailableMarkets:      []string{
                "available_markets8",
            },
            DiscNumber:            models.ToPointer(206),
            DurationMs:            models.ToPointer(142),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        PlayedAt:              models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
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
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



