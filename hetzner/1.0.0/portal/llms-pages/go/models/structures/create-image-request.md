# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `*string` | Optional | Description of the Image, will be auto-generated if not set |
| `Labels` | [`*models.Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `Type` | [`*models.Type63`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    createImageRequest := models.CreateImageRequest{
        Description:           models.ToPointer("my image"),
        Labels:                models.ToPointer(models.Labels{
            Labelkey:              models.ToPointer("labelkey4"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Type:                  models.ToPointer(models.Type63_Snapshot),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



