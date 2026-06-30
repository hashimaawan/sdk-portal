# Vault 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlZhdWx0MQ

*This model accepts additional fields of type interface{}.*


# Class Name

`Vault1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Required | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    vault1 := models.Vault1{
        Id:                    "id0",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



