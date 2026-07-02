# Session State

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0ZQ


# Class Name

`SessionState`


# Fields

| Name |
|  --- |
| `Creating` |
| `Created` |
| `Idle` |
| `Busy` |
| `Terminating` |
| `Terminated` |
| `Degraded` |
| `Failed` |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    sessionState := models.SessionState_Terminating

}
```



