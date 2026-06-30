# Saved Show Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlNhdmVkU2hvd09iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`SavedShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `*time.Time` | Optional | The date and time the show was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `Show` | [`*models.ShowBase`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/show-base.md) | Optional | Information about the show. |
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
    savedShowObject := models.SavedShowObject{
        AddedAt:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Show:                  models.ToPointer(models.ShowBase{
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
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



