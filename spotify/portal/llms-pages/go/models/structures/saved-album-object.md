# Saved Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlNhdmVkQWxidW1PYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`SavedAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `*time.Time` | Optional | The date and time the album was saved<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `Album` | [`*models.AlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/album-object.md) | Optional | Information about the album. |
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
    savedAlbumObject := models.SavedAlbumObject{
        AddedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Album:                 models.ToPointer(models.AlbumObject{
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
            Tracks:                models.PagingSimplifiedTrackObject{
                Href:                  "href6",
                Limit:                 142,
                Next:                  models.ToPointer("next8"),
                Offset:                238,
                Previous:              models.ToPointer("previous2"),
                Total:                 236,
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
                "genres5",
                "genres6",
                "genres7",
            },
            Label:                 "label8",
            Popularity:            78,
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



