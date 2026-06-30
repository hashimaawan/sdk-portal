# Cursor Paging Simplified Artist Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ1NpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`CursorPagingSimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `*string` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `Limit` | `*int` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `*string` | Optional | URL to the next page of items. ( `null` if none) |
| `Cursors` | [`*models.CursorObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `Total` | `*int` | Optional | The total number of items available to return. |
| `Items` | [`[]models.ArtistObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/artist-object.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    cursorPagingSimplifiedArtistObject := models.CursorPagingSimplifiedArtistObject{
        Href:                  models.ToPointer("href2"),
        Limit:                 models.ToPointer(24),
        Next:                  models.ToPointer("next2"),
        Cursors:               models.ToPointer(models.CursorObject{
            After:                 models.ToPointer("after8"),
            Before:                models.ToPointer("before6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Total:                 models.ToPointer(118),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



