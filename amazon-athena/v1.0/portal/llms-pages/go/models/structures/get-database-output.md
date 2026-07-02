# Get Database Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldERhdGFiYXNlT3V0cHV0

*This model accepts additional fields of type interface{}.*


# Class Name

`GetDatabaseOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | [`*models.Database2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/database-2.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    getDatabaseOutput := models.GetDatabaseOutput{
        Database:              models.ToPointer(models.Database2{
            Name:                  "Name2",
            Description:           models.ToPointer("Description8"),
            Parameters:            models.ToPointer(models.Parameters{
                AdditionalProperties:  map[string]string{
                    "exampleAdditionalProperty": "Parameters_additionalProperties2",
                },
            }),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



