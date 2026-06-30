# Playlist Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`PlaylistTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `*time.Time` | Optional | The date and time the track or episode was added. _**Note**: some very old playlists may return `null` in this field._ |
| `AddedBy` | [`*models.PlaylistUserObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/playlist-user-object.md) | Optional | The Spotify user who added the track or episode. _**Note**: some very old playlists may return `null` in this field._ |
| `IsLocal` | `*bool` | Optional | Whether this track or episode is a [local file](/documentation/web-api/concepts/playlists/#local-files) or not. |
| `Track` | [`*models.PlaylistTrackObjectTrack`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/oneof-anyof-definitions/playlist-track-object-track.md) | Optional | This is a container for one-of cases. |
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
    playlistTrackObject := models.PlaylistTrackObject{
        AddedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        AddedBy:               models.ToPointer(models.PlaylistUserObject{
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
            Href:                  models.ToPointer("href6"),
            Id:                    models.ToPointer("id4"),
            Type:                  models.ToPointer(models.Type3_User),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        IsLocal:               models.ToPointer(false),
        Track:                 models.ToPointer(models.PlaylistTrackObjectTrackContainer.FromTrackObject(models.TrackObject{
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



