# Saved Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRlNhdmVkVHJhY2tPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`SavedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `*time.Time` | Optional | The date and time the track was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `Track` | [`*models.TrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/track-object.md) | Optional | Information about the track. |
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
    savedTrackObject := models.SavedTrackObject{
        AddedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
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
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



