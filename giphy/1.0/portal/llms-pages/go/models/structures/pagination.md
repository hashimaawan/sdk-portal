# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/go/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions.

*This model accepts additional fields of type interface{}.*


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Count` | `*int` | Optional | Total number of items returned. |
| `Offset` | `*int` | Optional | Position in pagination. |
| `TotalCount` | `*int` | Optional | Total number of items available. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "giphyApi/models"
)

func main() {
    pagination := models.Pagination{
        Count:                 models.ToPointer(25),
        Offset:                models.ToPointer(75),
        TotalCount:            models.ToPointer(250),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



