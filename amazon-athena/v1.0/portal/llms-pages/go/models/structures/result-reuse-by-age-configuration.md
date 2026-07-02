# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.


# Class Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `bool` | Required | - |
| `MaxAgeInMinutes` | `*int` | Optional | **Constraints**: `>= 0`, `<= 10080` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    resultReuseByAgeConfiguration := models.ResultReuseByAgeConfiguration{
        Enabled:              false,
        MaxAgeInMinutes:      models.ToPointer(134),
    }

}
```



