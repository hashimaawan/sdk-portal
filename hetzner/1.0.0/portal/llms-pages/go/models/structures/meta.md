# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRk1ldGE

*This model accepts additional fields of type interface{}.*


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`models.Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/pagination.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    meta := models.Meta{
        Pagination:            models.Pagination{
            LastPage:              models.ToPointer(float64(4)),
            NextPage:              models.ToPointer(float64(4)),
            Page:                  float64(3),
            PerPage:               float64(25),
            PreviousPage:          models.ToPointer(float64(2)),
            TotalEntries:          models.ToPointer(float64(100)),
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



