# Patch

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlBhdGNo

*This model accepts additional fields of type interface{}.*


# Class Name

`Patch`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Op` | [`models.Op`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/op.md) | Required | - |
| `Path` | `string` | Required | An RFC6901 JSON Pointer pointing to the Item document, an Item Attribute, and Item Field by Field ID, or an Item Field Attribute |
| `Value` | `*interface{}` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    patch := models.Patch{
        Op:                    models.Op_Remove,
        Path:                  "/fields/06gnn2b95example10q91512p5/label",
        Value:                 models.ToPointer(interface{}("[key1, val1][key2, val2]")),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



