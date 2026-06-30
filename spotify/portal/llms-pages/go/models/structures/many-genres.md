# Many Genres

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRk1hbnlHZW5yZXM

*This model accepts additional fields of type interface{}.*


# Class Name

`ManyGenres`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Genres` | `[]string` | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    manyGenres := models.ManyGenres{
        Genres:                []string{
            "alternative",
            "samba",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



