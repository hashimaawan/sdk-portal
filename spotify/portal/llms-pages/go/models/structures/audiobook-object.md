# Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkF1ZGlvYm9va09iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`AudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Authors` | [`[]models.AuthorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/author-object.md) | Required | The author(s) for the audiobook. |
| `AvailableMarkets` | `[]string` | Required | A list of the countries in which the audiobook can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `Copyrights` | [`[]models.CopyrightObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/copyright-object.md) | Required | The copyright statements of the audiobook. |
| `Description` | `string` | Required | A description of the audiobook. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `HtmlDescription` | `string` | Required | A description of the audiobook. This field may contain HTML tags. |
| `Edition` | `*string` | Optional | The edition of the audiobook. |
| `Explicit` | `bool` | Required | Whether or not the audiobook has explicit content (true = yes it does; false = no it does not OR unknown). |
| `ExternalUrls` | [`models.ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/external-url-object.md) | Required | External URLs for this audiobook. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the audiobook. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `Images` | [`[]models.ImageObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/image-object.md) | Required | The cover art for the audiobook in various sizes, widest first. |
| `Languages` | `[]string` | Required | A list of the languages used in the audiobook, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `MediaType` | `string` | Required | The media type of the audiobook. |
| `Name` | `string` | Required | The name of the audiobook. |
| `Narrators` | [`[]models.NarratorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/narrator-object.md) | Required | The narrator(s) for the audiobook. |
| `Publisher` | `string` | Required | The publisher of the audiobook. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"audiobook"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `TotalChapters` | `int` | Required | The number of chapters in this audiobook. |
| `Chapters` | [`models.PagingSimplifiedChapterObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/paging-simplified-chapter-object.md) | Required | The chapters of the audiobook. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    audiobookObject := models.AudiobookObject{
        Authors:               []models.AuthorObject{
            models.AuthorObject{
                Name:                  models.ToPointer("name0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AvailableMarkets:      []string{
            "available_markets4",
            "available_markets5",
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
        Description:           "description0",
        HtmlDescription:       "html_description0",
        Edition:               models.ToPointer("Unabridged"),
        Explicit:              false,
        ExternalUrls:          models.ExternalUrlObject{
            Spotify:               models.ToPointer("spotify6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        Href:                  "href2",
        Id:                    "id0",
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
            "languages1",
            "languages2",
            "languages3",
        },
        MediaType:             "media_type2",
        Name:                  "name0",
        Narrators:             []models.NarratorObject{
            models.NarratorObject{
                Name:                  models.ToPointer("name0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Publisher:             "publisher2",
        Type:                  "audiobook",
        Uri:                   "uri4",
        TotalChapters:         72,
        Chapters:              models.PagingSimplifiedChapterObject{
            Href:                  "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
            Limit:                 20,
            Next:                  models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
            Offset:                0,
            Previous:              models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
            Total:                 4,
            Items:                 []models.ChapterBase{
                models.ChapterBase{
                    AudioPreviewUrl:       models.ToPointer("https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17"),
                    AvailableMarkets:      []string{
                        "available_markets2",
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



