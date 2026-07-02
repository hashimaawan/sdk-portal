# Query Runtime Statistics Rows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NSb3dz

Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query.

*This model accepts additional fields of type interface{}.*


# Class Name

`QueryRuntimeStatisticsRows`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InputRows` | `*int` | Optional | - |
| `InputBytes` | `*int` | Optional | - |
| `OutputBytes` | `*int` | Optional | - |
| `OutputRows` | `*int` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    queryRuntimeStatisticsRows := models.QueryRuntimeStatisticsRows{
        InputRows:             models.ToPointer(234),
        InputBytes:            models.ToPointer(254),
        OutputBytes:           models.ToPointer(40),
        OutputRows:            models.ToPointer(226),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



