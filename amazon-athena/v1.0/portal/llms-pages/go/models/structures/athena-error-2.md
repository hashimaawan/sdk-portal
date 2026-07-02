# Athena Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkF0aGVuYUVycm9yMg


# Class Name

`AthenaError2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ErrorCategory` | `*int` | Optional | **Constraints**: `>= 1`, `<= 3` |
| `ErrorType` | `*int` | Optional | **Constraints**: `>= 0`, `<= 9999` |
| `Retryable` | `*bool` | Optional | - |
| `ErrorMessage` | `*string` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    athenaError2 := models.AthenaError2{
        ErrorCategory:        models.ToPointer(3),
        ErrorType:            models.ToPointer(56),
        Retryable:            models.ToPointer(false),
        ErrorMessage:         models.ToPointer("ErrorMessage0"),
    }

}
```



