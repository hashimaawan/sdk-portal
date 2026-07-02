# Athena Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkF0aGVuYUVycm9y

Provides information about an Athena query error. The <code>AthenaError</code> feature provides standardized error information to help you understand failed queries and take steps after a query failure occurs. <code>AthenaError</code> includes an <code>ErrorCategory</code> field that specifies whether the cause of the failed query is due to system error, user error, or other error.

*This model accepts additional fields of type interface{}.*


# Class Name

`AthenaError`


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
    athenaError := models.AthenaError{
        ErrorCategory:         models.ToPointer(3),
        ErrorType:             models.ToPointer(238),
        Retryable:             models.ToPointer(false),
        ErrorMessage:          models.ToPointer("ErrorMessage0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



