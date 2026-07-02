# Session State

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0ZQ


# Class Name

`SessionStateEnum`


# Fields

| Name |
|  --- |
| `CREATING` |
| `CREATED` |
| `IDLE` |
| `BUSY` |
| `TERMINATING` |
| `TERMINATED` |
| `DEGRADED` |
| `FAILED` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    sessionState := models.SessionStateEnum_TERMINATING

}
```



