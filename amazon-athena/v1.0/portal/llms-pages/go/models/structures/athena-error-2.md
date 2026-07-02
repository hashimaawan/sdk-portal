# Athena Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkF0aGVuYUVycm9yMg

*This model accepts additional fields of type interface{}.*


# Class Name

`AthenaError2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ErrorCategory` | `*int` | Optional | **Constraints**: `>= 1`, `<= 3` |
| `ErrorType` | `*int` | Optional | **Constraints**: `>= 0`, `<= 9999` |
| `Retryable` | `*bool` | Optional | - |
| `ErrorMessage` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    athenaError2 := models.AthenaError2{
        ErrorCategory:         models.ToPointer(3),
        ErrorType:             models.ToPointer(56),
        Retryable:             models.ToPointer(false),
        ErrorMessage:          models.ToPointer("ErrorMessage0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



