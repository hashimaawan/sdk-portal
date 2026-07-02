# Unprocessed Prepared Statement Name

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUHJlcGFyZWRTdGF0ZW1lbnROYW1l

The name of a prepared statement that could not be returned.

*This model accepts additional fields of type interface{}.*


# Class Name

`UnprocessedPreparedStatementName`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StatementName` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `ErrorCode` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `ErrorMessage` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    unprocessedPreparedStatementName := models.UnprocessedPreparedStatementName{
        StatementName:         models.ToPointer("StatementName8"),
        ErrorCode:             models.ToPointer("ErrorCode6"),
        ErrorMessage:          models.ToPointer("ErrorMessage6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



