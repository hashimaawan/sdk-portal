# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `*string` | Optional | New description of Image |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Type` | [`*models.Type24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-24.md) | Optional | Destination Image type to convert to |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    updateImageRequest := models.UpdateImageRequest{
        Description:           models.ToPointer("My new Image description"),
        Labels:                models.ToPointer(interface{}("[labelkey, value]")),
        Type:                  models.ToPointer(models.Type24_Snapshot),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



