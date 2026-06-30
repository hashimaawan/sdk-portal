# Cursor Paging Play History Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ1BsYXlIaXN0b3J5T2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`CursorPagingPlayHistoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `*string` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `Limit` | `*int` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `*string` | Optional | URL to the next page of items. ( `null` if none) |
| `Cursors` | [`*models.CursorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `Total` | `*int` | Optional | The total number of items available to return. |
| `Items` | [`[]models.PlayHistoryObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/play-history-object.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    cursorPagingPlayHistoryObject := models.CursorPagingPlayHistoryObject{
        Href:                  models.ToPointer("href2"),
        Limit:                 models.ToPointer(124),
        Next:                  models.ToPointer("next8"),
        Cursors:               models.ToPointer(models.CursorObject{
            After:                 models.ToPointer("after8"),
            Before:                models.ToPointer("before6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Total:                 models.ToPointer(218),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



