# Protection 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByb3RlY3Rpb24xMQ

Protection configuration for the Network

*This model accepts additional fields of type interface{}.*


# Class Name

`Protection11`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool` | Required | If true, prevents the Network from being deleted |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    protection11 := models.Protection11{
        Delete:                false,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



