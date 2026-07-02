# Datum

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkRhdHVt

A piece of data (a field in the table).

*This model accepts additional fields of type interface{}.*


# Class Name

`Datum`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `VarCharValue` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    datum := models.Datum{
        VarCharValue:          models.ToPointer("VarCharValue8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



