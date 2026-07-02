# Result Reuse by Age Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9uMg

*This model accepts additional fields of type interface{}.*


# Class Name

`ResultReuseByAgeConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `bool` | Required | - |
| `MaxAgeInMinutes` | `*int` | Optional | **Constraints**: `>= 0`, `<= 10080` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    resultReuseByAgeConfiguration2 := models.ResultReuseByAgeConfiguration2{
        Enabled:               false,
        MaxAgeInMinutes:       models.ToPointer(44),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



