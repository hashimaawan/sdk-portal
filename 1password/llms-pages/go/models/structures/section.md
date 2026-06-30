# Section

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlNlY3Rpb24

*This model accepts additional fields of type interface{}.*


# Class Name

`Section`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    section := models.Section{
        Id:                    models.ToPointer("id6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



