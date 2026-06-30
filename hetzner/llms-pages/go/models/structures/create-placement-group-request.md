# Create Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA


# Class Name

`CreatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the PlacementGroup |
| `Type` | `string` | Required, Constant | Define the Placement Group Type.<br><br>**Value**: `"spread"` |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createPlacementGroupRequest := models.CreatePlacementGroupRequest{
        Labels:               models.ToPointer(interface{}("[key1, val1][key2, val2]")),
        Name:                 "my Placement Group",
        Type:                 "spread",
    }

}
```



