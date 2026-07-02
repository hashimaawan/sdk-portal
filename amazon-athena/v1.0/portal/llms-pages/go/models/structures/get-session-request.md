# Get Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXF1ZXN0


# Class Name

`GetSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getSessionRequest := models.GetSessionRequest{
        SessionId:            "SessionId2",
    }

}
```



