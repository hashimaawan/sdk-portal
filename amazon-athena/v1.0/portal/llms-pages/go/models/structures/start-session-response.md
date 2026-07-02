# Start Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlc3BvbnNl


# Class Name

`StartSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `State` | [`*models.SessionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/session-state-1.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    startSessionResponse := models.StartSessionResponse{
        SessionId:            models.ToPointer("SessionId4"),
        State:                models.ToPointer(models.SessionState1Enum_CREATING),
    }

}
```



