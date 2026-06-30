# Copyright Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRkNvcHlyaWdodE9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`CopyrightObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Text` | `*string` | Optional | The copyright text for this content. |
| `Type` | `*string` | Optional | The type of copyright: `C` = the copyright, `P` = the sound recording (performance) copyright. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    copyrightObject := models.CopyrightObject{
        Text:                  models.ToPointer("text4"),
        Type:                  models.ToPointer("type4"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



