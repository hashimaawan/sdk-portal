# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.


# Class Name

`CalculationConfiguration`


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
    calculationConfiguration := models.CalculationConfiguration{
        CodeBlock:            models.ToPointer("CodeBlock2"),
    }

}
```



