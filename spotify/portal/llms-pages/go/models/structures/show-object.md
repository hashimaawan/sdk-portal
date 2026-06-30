# Show Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRlNob3dPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`ShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AvailableMarkets` | `[]string` | Required | A list of the countries in which the show can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `Copyrights` | [`[]models.CopyrightObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/copyright-object.md) | Required | The copyright statements of the show. |
| `Description` | `string` | Required | A description of the show. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `HtmlDescription` | `string` | Required | A description of the show. This field may contain HTML tags. |
| `Explicit` | `bool` | Required | Whether or not the show has explicit content (true = yes it does; false = no it does not OR unknown). |
| `ExternalUrls` | [`models.ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/external-url-object.md) | Required | External URLs for this show. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the show. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `Images` | [`[]models.ImageObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/image-object.md) | Required | The cover art for the show in various sizes, widest first. |
| `IsExternallyHosted` | `bool` | Required | True if all of the shows episodes are hosted outside of Spotify's CDN. This field might be `null` in some cases. |
| `Languages` | `[]string` | Required | A list of the languages used in the show, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `MediaType` | `string` | Required | The media type of the show. |
| `Name` | `string` | Required | The name of the episode. |
| `Publisher` | `string` | Required | The publisher of the show. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"show"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `TotalEpisodes` | `int` | Required | The total number of episodes in the show. |
| `Episodes` | [`models.PagingSimplifiedEpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/paging-simplified-episode-object.md) | Required | The episodes of the show. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    showObject := models.ShowObject{
        AvailableMarkets:      []string{
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
        Description:           "description8",
        HtmlDescription:       "html_description8",
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
        IsExternallyHosted:    false,
        Languages:             []string{
            "languages5",
        },
        MediaType:             "media_type6",
        Name:                  "name8",
        Publisher:             "publisher6",
        Type:                  "show",
        Uri:                   "uri2",
        TotalEpisodes:         230,
        Episodes:              models.PagingSimplifiedEpisodeObject{
            Href:                  "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
            Limit:                 20,
            Next:                  models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
            Offset:                0,
            Previous:              models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
            Total:                 4,
            Items:                 []models.EpisodeBase{
                models.EpisodeBase{
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
    }

}
```



