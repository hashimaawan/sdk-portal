# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server

*This model accepts additional fields of type interface{}.*


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool` | Required | If true, prevents the Server from being deleted |
| `Rebuild` | `bool` | Required | If true, prevents the Server from being rebuilt |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    protection20 := models.Protection20{
        Delete:                false,
        Rebuild:               false,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



