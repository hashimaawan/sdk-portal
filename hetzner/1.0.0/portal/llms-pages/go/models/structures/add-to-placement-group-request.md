# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PlacementGroup` | `int` | Required | ID of Placement Group the Server should be added to |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    addToPlacementGroupRequest := models.AddToPlacementGroupRequest{
        PlacementGroup:       1,
    }

}
```



