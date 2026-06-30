# Saved Episode Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlNhdmVkRXBpc29kZU9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`SavedEpisodeObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `*time.Time` | Optional | The date and time the episode was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ. |
| `Episode` | [`*models.EpisodeObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/episode-object.md) | Optional | Information about the episode. |
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
    savedEpisodeObject := models.SavedEpisodeObject{
        AddedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Episode:               models.ToPointer(models.EpisodeObject{
            AudioPreviewUrl:       models.ToPointer("audio_preview_url8"),
            Description:           "description2",
            HtmlDescription:       "html_description8",
            DurationMs:            46,
            Explicit:              false,
            ExternalUrls:          models.ExternalUrlObject{
                Spotify:               models.ToPointer("spotify6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            Href:                  "href4",
            Id:                    "id2",
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
            IsExternallyHosted:    false,
            IsPlayable:            false,
            Language:              models.ToPointer("language4"),
            Languages:             []string{
                "languages9",
                "languages0",
                "languages1",
            },
            Name:                  "name2",
            ReleaseDate:           "release_date0",
            ReleaseDatePrecision:  models.ReleaseDatePrecision_Year,
            ResumePoint:           models.ToPointer(models.ResumePointObject{
                FullyPlayed:           models.ToPointer(false),
                ResumePositionMs:      models.ToPointer(254),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Type:                  "type8",
            Uri:                   "uri6",
            Restrictions:          models.ToPointer(models.EpisodeRestrictionObject{
                Reason:                models.ToPointer("reason0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Show:                  models.ShowBase{
                AvailableMarkets:      []string{
                    "available_markets0",
                    "available_markets1",
                    "available_markets2",
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
                Description:           "description4",
                HtmlDescription:       "html_description4",
                Explicit:              false,
                ExternalUrls:          models.ExternalUrlObject{
                    Spotify:               models.ToPointer("spotify6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Href:                  "href8",
                Id:                    "id6",
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
                IsExternallyHosted:    false,
                Languages:             []string{
                    "languages7",
                    "languages6",
                    "languages5",
                },
                MediaType:             "media_type6",
                Name:                  "name6",
                Publisher:             "publisher6",
                Type:                  "type4",
                Uri:                   "uri0",
                TotalEpisodes:         198,
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



