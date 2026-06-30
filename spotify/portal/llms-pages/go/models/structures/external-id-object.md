# External Id Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkV4dGVybmFsSWRPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`ExternalIdObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Isrc` | `*string` | Optional | [International Standard Recording Code](http://en.wikipedia.org/wiki/International_Standard_Recording_Code) |
| `Ean` | `*string` | Optional | [International Article Number](http://en.wikipedia.org/wiki/International_Article_Number_%28EAN%29) |
| `Upc` | `*string` | Optional | [Universal Product Code](http://en.wikipedia.org/wiki/Universal_Product_Code) |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    externalIdObject := models.ExternalIdObject{
        Isrc:                  models.ToPointer("isrc4"),
        Ean:                   models.ToPointer("ean2"),
        Upc:                   models.ToPointer("upc6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



