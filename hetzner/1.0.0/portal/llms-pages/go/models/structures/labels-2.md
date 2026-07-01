# Labels 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxhYmVsczI

User-defined labels (key-value pairs)

*This model accepts additional fields of type interface{}.*


# Class Name

`Labels2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labelkey` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    labels2 := models.Labels2{
        Labelkey:              models.ToPointer("value"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



