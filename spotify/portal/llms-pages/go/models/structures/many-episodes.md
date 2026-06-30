# Many Episodes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRk1hbnlFcGlzb2Rlcw

*This model accepts additional fields of type interface{}.*


# Class Name

`ManyEpisodes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Episodes` | [`[]models.EpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/episode-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    manyEpisodes := models.ManyEpisodes{
        Episodes:              []models.EpisodeObject{
            models.EpisodeObject{
                AudioPreviewUrl:       models.ToPointer("https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17"),
                Description:           "A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.\n",
                HtmlDescription:       "<p>A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.</p>\n",
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
                IsExternallyHosted:    false,
                IsPlayable:            false,
                Language:              models.ToPointer("en"),
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
                            Url:                   "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                            Height:                models.ToPointer(300),
                            Width:                 models.ToPointer(300),
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
                    Type:                  "show",
                    Uri:                   "uri0",
                    TotalEpisodes:         198,
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



