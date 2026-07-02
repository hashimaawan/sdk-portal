# Result Reuse Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbjE


# Class Name

`ResultReuseConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResultReuseByAgeConfiguration` | [`*models.ResultReuseByAgeConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    resultReuseConfiguration1 := models.ResultReuseConfiguration1{
        ResultReuseByAgeConfiguration: models.ToPointer(models.ResultReuseByAgeConfiguration2{
            Enabled:              false,
            MaxAgeInMinutes:      models.ToPointer(26),
        }),
    }

}
```



