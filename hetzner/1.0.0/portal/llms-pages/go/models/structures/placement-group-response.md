# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Class Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PlacementGroup` | [`models.PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/placement-group.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    placementGroupResponse := models.PlacementGroupResponse{
        PlacementGroup:       models.PlacementGroup{
            Created:              "2016-01-30T23:55:00+00:00",
            Id:                   42,
            Labels:               map[string]string{
                "key0": "labels4",
            },
            Name:                 "my-resource",
            Servers:              []int{
                42,
            },
            Type:                 "spread",
        },
    }

}
```



