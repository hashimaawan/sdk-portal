# Item 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRkl0ZW0y

*This model accepts additional fields of type interface{}.*


# Class Name

`Item2`


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
    item2 := models.Item2{
        Id:                    models.ToPointer("id2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



