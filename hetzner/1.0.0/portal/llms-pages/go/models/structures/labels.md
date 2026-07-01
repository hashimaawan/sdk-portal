# Labels

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxhYmVscw

User-defined labels (key-value pairs)

*This model accepts additional fields of type interface{}.*


# Class Name

`Labels`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labelkey` | `*string` | Optional | New label |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    labels := models.Labels{
        Labelkey:              models.ToPointer("value"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



