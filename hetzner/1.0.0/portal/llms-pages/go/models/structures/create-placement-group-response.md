# Create Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`CreatePlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`models.Optional[models.NullableAction]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/nullable-action.md) | Optional | - |
| `PlacementGroup` | [`models.PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/placement-group.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    createPlacementGroupResponse := models.CreatePlacementGroupResponse{
        Action:                models.NewOptional(models.ToPointer(models.NullableAction{
            Command:               "command6",
            Error:                 models.ToPointer(models.Error{
                Code:                  "code2",
                Message:               "message4",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Finished:              models.ToPointer("finished0"),
            Id:                    238,
            Progress:              float64(143.26),
            Resources:             []models.Resource{
                models.Resource{
                    Id:                    198,
                    Type:                  "type0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Resource{
                    Id:                    198,
                    Type:                  "type0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Resource{
                    Id:                    198,
                    Type:                  "type0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Started:               "started8",
            Status:                models.Status_Running,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        })),
        PlacementGroup:        models.PlacementGroup{
            Created:               "2016-01-30T23:55:00+00:00",
            Id:                    42,
            Labels:                map[string]string{
                "key0": "labels4",
            },
            Name:                  "my-resource",
            Servers:               []int{
                42,
            },
            Type:                  "spread",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



