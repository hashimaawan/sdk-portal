# Label Selector 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3Ix

Configuration for type LabelSelector, required if type is `label_selector`

*This model accepts additional fields of type interface{}.*


# Class Name

`LabelSelector1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Selector` | `string` | Required | Label selector |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    labelSelector1 := models.LabelSelector1{
        Selector:              "selector2",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



