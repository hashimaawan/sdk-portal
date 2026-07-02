# Result Reuse Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbg

Specifies the query result reuse behavior for the query.

*This model accepts additional fields of type interface{}.*


# Class Name

`ResultReuseConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResultReuseByAgeConfiguration` | [`*models.ResultReuseByAgeConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    resultReuseConfiguration := models.ResultReuseConfiguration{
        ResultReuseByAgeConfiguration: models.ToPointer(models.ResultReuseByAgeConfiguration2{
            Enabled:               false,
            MaxAgeInMinutes:       models.ToPointer(26),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:          map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



