# Datum

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkRhdHVt

A piece of data (a field in the table).


# Class Name

`Datum`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `VarCharValue` | `*string` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    datum := models.Datum{
        VarCharValue:         models.ToPointer("VarCharValue8"),
    }

}
```



