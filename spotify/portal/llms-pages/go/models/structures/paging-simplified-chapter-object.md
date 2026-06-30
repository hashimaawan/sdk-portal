# Paging Simplified Chapter Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlBhZ2luZ1NpbXBsaWZpZWRDaGFwdGVyT2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`PagingSimplifiedChapterObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `Limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `*string` | Required | URL to the next page of items. ( `null` if none) |
| `Offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `Previous` | `*string` | Required | URL to the previous page of items. ( `null` if none) |
| `Total` | `int` | Required | The total number of items available to return. |
| `Items` | [`[]models.ChapterBase`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/chapter-base.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    pagingSimplifiedChapterObject := models.PagingSimplifiedChapterObject{
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
    }

}
```



