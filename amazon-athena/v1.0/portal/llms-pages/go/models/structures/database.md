# Database

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkRhdGFiYXNl

Contains metadata information for a database in a data catalog.

*This model accepts additional fields of type interface{}.*


# Class Name

`Database`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `Parameters` | [`*models.Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/parameters.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    database := models.Database{
        Name:                  "Name0",
        Description:           models.ToPointer("Description6"),
        Parameters:            models.ToPointer(models.Parameters{
            AdditionalProperties:  map[string]string{
                "exampleAdditionalProperty": "Parameters_additionalProperties2",
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



