# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.

*This model accepts additional fields of type interface{}.*


# Class Name

`CalculationConfiguration`


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
    calculationConfiguration := models.CalculationConfiguration{
        CodeBlock:             models.ToPointer("CodeBlock2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



