# Session Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0aXN0aWNz

Contains statistics for a session.


# Class Name

`SessionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DpuExecutionInMillis` | `*int` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    sessionStatistics := models.SessionStatistics{
        DpuExecutionInMillis: models.ToPointer(188),
    }

}
```



