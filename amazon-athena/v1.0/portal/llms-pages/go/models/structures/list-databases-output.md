# List Databases Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNPdXRwdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ListDatabasesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DatabaseList` | [`[]models.Database`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/database.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listDatabasesOutput := models.ListDatabasesOutput{
        DatabaseList:          []models.Database{
            models.Database{
                Name:                  "Name4",
                Description:           models.ToPointer("Description8"),
                Parameters:            models.ToPointer(models.Parameters{
                    AdditionalProperties:  map[string]string{
                        "exampleAdditionalProperty": "Parameters_additionalProperties2",
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Database{
                Name:                  "Name4",
                Description:           models.ToPointer("Description8"),
                Parameters:            models.ToPointer(models.Parameters{
                    AdditionalProperties:  map[string]string{
                        "exampleAdditionalProperty": "Parameters_additionalProperties2",
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Database{
                Name:                  "Name4",
                Description:           models.ToPointer("Description8"),
                Parameters:            models.ToPointer(models.Parameters{
                    AdditionalProperties:  map[string]string{
                        "exampleAdditionalProperty": "Parameters_additionalProperties2",
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        NextToken:             models.ToPointer("NextToken6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



