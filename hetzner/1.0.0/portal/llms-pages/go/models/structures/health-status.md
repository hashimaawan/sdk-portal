# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw

*This model accepts additional fields of type interface{}.*


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ListenPort` | `*int` | Optional | - |
| `Status` | [`*models.Status30`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/status-30.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    healthStatus := models.HealthStatus{
        ListenPort:            models.ToPointer(443),
        Status:                models.ToPointer(models.Status30_Healthy),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



