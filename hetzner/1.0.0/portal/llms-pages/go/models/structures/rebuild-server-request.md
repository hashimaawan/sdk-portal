# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0

*This model accepts additional fields of type interface{}.*


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Image` | `string` | Required | ID or name of Image to rebuilt from. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    rebuildServerRequest := models.RebuildServerRequest{
        Image:                 "ubuntu-20.04",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



