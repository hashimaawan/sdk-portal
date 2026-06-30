# Cursor Paging Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ09iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`CursorPagingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `*string` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `Limit` | `*int` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `*string` | Optional | URL to the next page of items. ( `null` if none) |
| `Cursors` | [`*models.CursorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `Total` | `*int` | Optional | The total number of items available to return. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    cursorPagingObject := models.CursorPagingObject{
        Href:                  models.ToPointer("href8"),
        Limit:                 models.ToPointer(82),
        Next:                  models.ToPointer("next6"),
        Cursors:               models.ToPointer(models.CursorObject{
            After:                 models.ToPointer("after8"),
            Before:                models.ToPointer("before6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Total:                 models.ToPointer(176),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



