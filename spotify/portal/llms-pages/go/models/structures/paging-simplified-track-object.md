# Paging Simplified Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlBhZ2luZ1NpbXBsaWZpZWRUcmFja09iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`PagingSimplifiedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `Limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `*string` | Required | URL to the next page of items. ( `null` if none) |
| `Offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `Previous` | `*string` | Required | URL to the previous page of items. ( `null` if none) |
| `Total` | `int` | Required | The total number of items available to return. |
| `Items` | [`[]models.SimplifiedTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/simplified-track-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    pagingSimplifiedTrackObject := models.PagingSimplifiedTrackObject{
        Href:                  "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
        Limit:                 20,
        Next:                  models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
        Offset:                0,
        Previous:              models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
        Total:                 4,
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
    }

}
```



