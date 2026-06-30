# Cursor Paged Artists

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkN1cnNvclBhZ2VkQXJ0aXN0cw

*This model accepts additional fields of type interface{}.*


# Class Name

`CursorPagedArtists`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Artists` | [`models.CursorPagingSimplifiedArtistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/cursor-paging-simplified-artist-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    cursorPagedArtists := models.CursorPagedArtists{
        Artists:               models.CursorPagingSimplifiedArtistObject{
            Href:                  models.ToPointer("href2"),
            Limit:                 models.ToPointer(214),
            Next:                  models.ToPointer("next2"),
            Cursors:               models.ToPointer(models.CursorObject{
                After:                 models.ToPointer("after8"),
                Before:                models.ToPointer("before6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Total:                 models.ToPointer(52),
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



