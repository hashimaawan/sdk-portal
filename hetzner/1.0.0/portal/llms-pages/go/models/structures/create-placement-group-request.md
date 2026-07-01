# Create Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`CreatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the PlacementGroup |
| `Type` | `string` | Required, Constant | Define the Placement Group Type.<br><br>**Value**: `"spread"` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    createPlacementGroupRequest := models.CreatePlacementGroupRequest{
        Labels:                models.ToPointer(interface{}("[key1, val1][key2, val2]")),
        Name:                  "my Placement Group",
        Type:                  "spread",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



