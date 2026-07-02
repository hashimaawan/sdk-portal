# Batch Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeU91dHB1dA

*This model accepts additional fields of type interface{}.*


# Class Name

`BatchGetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueries` | [`[]models.NamedQuery`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/named-query.md) | Optional | - |
| `UnprocessedNamedQueryIds` | [`[]models.UnprocessedNamedQueryId`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/unprocessed-named-query-id.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    batchGetNamedQueryOutput := models.BatchGetNamedQueryOutput{
        NamedQueries:             []models.NamedQuery{
            models.NamedQuery{
                Name:                  "Name2",
                Description:           models.ToPointer("Description4"),
                Database:              "Database0",
                QueryString:           "QueryString4",
                NamedQueryId:          models.ToPointer("NamedQueryId0"),
                WorkGroup:             models.ToPointer("WorkGroup4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.NamedQuery{
                Name:                  "Name2",
                Description:           models.ToPointer("Description4"),
                Database:              "Database0",
                QueryString:           "QueryString4",
                NamedQueryId:          models.ToPointer("NamedQueryId0"),
                WorkGroup:             models.ToPointer("WorkGroup4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.NamedQuery{
                Name:                  "Name2",
                Description:           models.ToPointer("Description4"),
                Database:              "Database0",
                QueryString:           "QueryString4",
                NamedQueryId:          models.ToPointer("NamedQueryId0"),
                WorkGroup:             models.ToPointer("WorkGroup4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        UnprocessedNamedQueryIds: []models.UnprocessedNamedQueryId{
            models.UnprocessedNamedQueryId{
                NamedQueryId:          models.ToPointer("NamedQueryId4"),
                ErrorCode:             models.ToPointer("ErrorCode6"),
                ErrorMessage:          models.ToPointer("ErrorMessage4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.UnprocessedNamedQueryId{
                NamedQueryId:          models.ToPointer("NamedQueryId4"),
                ErrorCode:             models.ToPointer("ErrorCode6"),
                ErrorMessage:          models.ToPointer("ErrorMessage4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:     map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



