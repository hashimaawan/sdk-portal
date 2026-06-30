# Cursor Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkN1cnNvck9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`CursorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `After` | `*string` | Optional | The cursor to use as key to find the next page of items. |
| `Before` | `*string` | Optional | The cursor to use as key to find the previous page of items. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    cursorObject := models.CursorObject{
        After:                 models.ToPointer("after0"),
        Before:                models.ToPointer("before8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



