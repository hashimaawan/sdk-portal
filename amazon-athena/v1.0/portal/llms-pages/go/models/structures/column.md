# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.

*This model accepts additional fields of type interface{}.*


# Class Name

`Column`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Type` | `*string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` |
| `Comment` | `*string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    column := models.Column{
        Name:                  "Name6",
        Type:                  models.ToPointer("Type6"),
        Comment:               models.ToPointer("Comment2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



