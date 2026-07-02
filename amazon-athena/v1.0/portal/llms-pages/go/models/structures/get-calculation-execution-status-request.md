# Get Calculation Execution Status Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVxdWVzdA


# Class Name

`GetCalculationExecutionStatusRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CalculationExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getCalculationExecutionStatusRequest := models.GetCalculationExecutionStatusRequest{
        CalculationExecutionId: "CalculationExecutionId8",
    }

}
```



