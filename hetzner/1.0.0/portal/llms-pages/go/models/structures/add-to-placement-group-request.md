# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0

*This model accepts additional fields of type interface{}.*


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PlacementGroup` | `int` | Required | ID of Placement Group the Server should be added to |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    addToPlacementGroupRequest := models.AddToPlacementGroupRequest{
        PlacementGroup:        1,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



