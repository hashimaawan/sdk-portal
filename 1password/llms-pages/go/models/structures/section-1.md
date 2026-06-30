# Section 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlNlY3Rpb24x

For files that are in a section, this field describes the section.

*This model accepts additional fields of type interface{}.*


# Class Name

`Section1`


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
    section1 := models.Section1{
        Id:                    models.ToPointer("id2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



