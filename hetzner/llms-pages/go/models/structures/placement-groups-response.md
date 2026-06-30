# Placement Groups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vwc1Jlc3BvbnNl


# Class Name

`PlacementGroupsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/meta.md) | Optional | - |
| `PlacementGroups` | [`[]models.PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/placement-group.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    placementGroupsResponse := models.PlacementGroupsResponse{
        Meta:                 models.ToPointer(models.Meta{
            Pagination:           models.Pagination{
                LastPage:             models.ToPointer(float64(77.7)),
                NextPage:             models.ToPointer(float64(209.18)),
                Page:                 float64(17.58),
                PerPage:              float64(13.34),
                PreviousPage:         models.ToPointer(float64(50.02)),
                TotalEntries:         models.ToPointer(float64(206.64)),
            },
        }),
        PlacementGroups:      []models.PlacementGroup{
            models.PlacementGroup{
                Created:              "2016-01-30T23:55:00+00:00",
                Id:                   42,
                Labels:               map[string]string{
                    "key0": "labels0",
                    "key1": "labels1",
                },
                Name:                 "my-resource",
                Servers:              []int{
                    42,
                },
                Type:                 "spread",
            },
        },
    }

}
```



