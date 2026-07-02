# Result Reuse Information 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24y

*This model accepts additional fields of type interface{}.*


# Class Name

`ResultReuseInformation2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ReusedPreviousResult` | `bool` | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    resultReuseInformation2 := models.ResultReuseInformation2{
        ReusedPreviousResult:  false,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



