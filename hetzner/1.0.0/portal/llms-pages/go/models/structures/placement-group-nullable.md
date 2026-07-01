# Placement Group Nullable

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwTnVsbGFibGU

*This model accepts additional fields of type interface{}.*


# Class Name

`PlacementGroupNullable`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Id` | `int` | Required | ID of the Resource |
| `Labels` | `map[string]string` | Required | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `Servers` | `[]int` | Required | Array of IDs of Servers that are part of this Placement Group |
| `Type` | `string` | Required, Constant | Type of the Placement Group<br><br>**Value**: `"spread"` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    placementGroupNullable := models.PlacementGroupNullable{
        Created:               "2016-01-30T23:55:00+00:00",
        Id:                    42,
        Labels:                map[string]string{
            "key0": "labels2",
        },
        Name:                  "my-resource",
        Servers:               []int{
            42,
        },
        Type:                  "spread",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



