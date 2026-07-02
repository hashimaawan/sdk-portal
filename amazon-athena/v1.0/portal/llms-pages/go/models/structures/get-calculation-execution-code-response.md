# Get Calculation Execution Code Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlc3BvbnNl


# Class Name

`GetCalculationExecutionCodeResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CodeBlock` | `*string` | Optional | **Constraints**: *Maximum Length*: `68000` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getCalculationExecutionCodeResponse := models.GetCalculationExecutionCodeResponse{
        CodeBlock:            models.ToPointer("CodeBlock4"),
    }

}
```



