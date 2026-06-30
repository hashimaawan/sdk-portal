# Many Chapters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRk1hbnlDaGFwdGVycw

*This model accepts additional fields of type interface{}.*


# Class Name

`ManyChapters`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Chapters` | [`[]models.ChapterObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/chapter-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    manyChapters := models.ManyChapters{
        Chapters:              []models.ChapterObject{
            models.ChapterObject{
                AudioPreviewUrl:       models.ToPointer("https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17"),
                AvailableMarkets:      []string{
                    "available_markets6",
                    "available_markets7",
                },
                ChapterNumber:         1,
                Description:           "We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.\n",
                HtmlDescription:       "<p>We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.</p>\n",
                DurationMs:            1686230,
                Explicit:              false,
                ExternalUrls:          models.ExternalUrlObject{
                    Spotify:               models.ToPointer("spotify6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Href:                  "https://api.spotify.com/v1/episodes/5Xt5DXGzch68nYYamXrNxZ",
                Id:                    "5Xt5DXGzch68nYYamXrNxZ",
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
                IsPlayable:            false,
                Languages:             []string{
                    "fr",
                    "en",
                },
                Name:                  "Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators\n",
                ReleaseDate:           "1981-12-15",
                ReleaseDatePrecision:  models.ReleaseDatePrecision_Day,
                ResumePoint:           models.ToPointer(models.ResumePointObject{
                    FullyPlayed:           models.ToPointer(false),
                    ResumePositionMs:      models.ToPointer(254),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Type:                  "episode",
                Uri:                   "spotify:episode:0zLhl3WsOCQHbe1BPTiHgr",
                Restrictions:          models.ToPointer(models.ChapterRestrictionObject{
                    Reason:                models.ToPointer("reason0"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Audiobook:             models.AudiobookBase{
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
                    },
                    Description:           "description2",
                    HtmlDescription:       "html_description2",
                    Edition:               models.ToPointer("Unabridged"),
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
                            Url:                   "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                            Height:                models.ToPointer(300),
                            Width:                 models.ToPointer(300),
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
                    },
                    Publisher:             "publisher4",
                    Type:                  "audiobook",
                    Uri:                   "uri2",
                    TotalChapters:         186,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
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



