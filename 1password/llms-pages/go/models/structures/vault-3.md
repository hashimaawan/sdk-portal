# Vault 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlZhdWx0Mw

*This model accepts additional fields of type interface{}.*


# Class Name

`Vault3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `*string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    vault3 := models.Vault3{
        Id:                    models.ToPointer("id0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



