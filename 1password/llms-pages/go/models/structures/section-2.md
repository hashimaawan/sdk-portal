# Section 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlNlY3Rpb24y

*This model accepts additional fields of type interface{}.*


# Class Name

`Section2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `*string` | Optional | - |
| `Label` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    section2 := models.Section2{
        Id:                    models.ToPointer("id4"),
        Label:                 models.ToPointer("label4"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



