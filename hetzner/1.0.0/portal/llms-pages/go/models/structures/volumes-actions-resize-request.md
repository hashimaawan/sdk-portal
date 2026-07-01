# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Size` | `float64` | Required | New Volume size in GB (must be greater than current size) |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    volumesActionsResizeRequest := models.VolumesActionsResizeRequest{
        Size:                  float64(50),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



