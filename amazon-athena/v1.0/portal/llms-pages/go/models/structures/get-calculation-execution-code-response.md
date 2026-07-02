# Get Calculation Execution Code Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlc3BvbnNl

*This model accepts additional fields of type interface{}.*


# Class Name

`GetCalculationExecutionCodeResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CodeBlock` | `*string` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    getCalculationExecutionCodeResponse := models.GetCalculationExecutionCodeResponse{
        CodeBlock:             models.ToPointer("CodeBlock4"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



