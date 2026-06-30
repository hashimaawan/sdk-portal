# Saved Audiobook Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlNhdmVkQXVkaW9ib29rT2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`SavedAudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `*time.Time` | Optional | The date and time the audiobook was saved<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `Audiobook` | [`*models.AudiobookObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/audiobook-object.md) | Optional | Information about the audiobook. |
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
    savedAudiobookObject := models.SavedAudiobookObject{
        AddedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Audiobook:             models.ToPointer(models.AudiobookObject{
            Authors:               []models.AuthorObject{
                models.AuthorObject{
                    Name:                  models.ToPointer("name0"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AvailableMarkets:      []string{
                "available_markets2",
                "available_markets3",
                "available_markets4",
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
                models.CopyrightObject{
                    Text:                  models.ToPointer("text2"),
                    Type:                  models.ToPointer("type2"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Description:           "description2",
            HtmlDescription:       "html_description2",
            Edition:               models.ToPointer("edition8"),
            Explicit:              false,
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
                models.ImageObject{
                    Url:                   "url6",
                    Height:                models.ToPointer(182),
                    Width:                 models.ToPointer(222),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.ImageObject{
                    Url:                   "url6",
                    Height:                models.ToPointer(182),
                    Width:                 models.ToPointer(222),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Languages:             []string{
                "languages3",
                "languages4",
            },
            MediaType:             "media_type4",
            Name:                  "name8",
            Narrators:             []models.NarratorObject{
                models.NarratorObject{
                    Name:                  models.ToPointer("name0"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.NarratorObject{
                    Name:                  models.ToPointer("name0"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Publisher:             "publisher4",
            Type:                  "type2",
            Uri:                   "uri2",
            TotalChapters:         186,
            Chapters:              models.PagingSimplifiedChapterObject{
                Href:                  "href4",
                Limit:                 230,
                Next:                  models.ToPointer("next0"),
                Offset:                122,
                Previous:              models.ToPointer("previous0"),
                Total:                 136,
                Items:                 []models.ChapterBase{
                    models.ChapterBase{
                        AudioPreviewUrl:       models.ToPointer("audio_preview_url4"),
                        AvailableMarkets:      []string{
                            "available_markets2",
                        },
                        ChapterNumber:         164,
                        Description:           "description2",
                        HtmlDescription:       "html_description2",
                        DurationMs:            52,
                        Explicit:              false,
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
                            models.ImageObject{
                                Url:                   "url6",
                                Height:                models.ToPointer(182),
                                Width:                 models.ToPointer(222),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                        },
                        IsPlayable:            false,
                        Languages:             []string{
                            "languages5",
                        },
                        Name:                  "name8",
                        ReleaseDate:           "release_date6",
                        ReleaseDatePrecision:  models.ReleaseDatePrecision_Month,
                        ResumePoint:           models.ToPointer(models.ResumePointObject{
                            FullyPlayed:           models.ToPointer(false),
                            ResumePositionMs:      models.ToPointer(254),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        Type:                  "type2",
                        Uri:                   "uri2",
                        Restrictions:          models.ToPointer(models.ChapterRestrictionObject{
                            Reason:                models.ToPointer("reason0"),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
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



