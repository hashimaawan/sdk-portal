# Statistics 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mx


# Class Name

`Statistics1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DpuExecutionInMillis` | `*int` | Optional | - |
| `Progress` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    statistics1 := models.Statistics1{
        DpuExecutionInMillis: models.ToPointer(148),
        Progress:             models.ToPointer("Progress4"),
    }

}
```



