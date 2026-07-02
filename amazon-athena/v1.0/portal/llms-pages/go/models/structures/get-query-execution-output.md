# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0

*This model accepts additional fields of type interface{}.*


# Class Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecution` | [`*models.QueryExecution1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-execution-1.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    getQueryExecutionOutput := models.GetQueryExecutionOutput{
        QueryExecution:        models.ToPointer(models.QueryExecution1{
            QueryExecutionId:         models.ToPointer("QueryExecutionId0"),
            Query:                    models.ToPointer("Query6"),
            StatementType:            models.ToPointer(models.StatementType1_Ddl),
            ResultConfiguration:      models.ToPointer(models.ResultConfiguration1{
                OutputLocation:          models.ToPointer("OutputLocation0"),
                EncryptionConfiguration: models.ToPointer(models.EncryptionConfiguration2{
                    EncryptionOption:      models.EncryptionOption1_SseS3,
                    KmsKey:                models.ToPointer("KmsKey6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                ExpectedBucketOwner:     models.ToPointer("ExpectedBucketOwner0"),
                AclConfiguration:        models.ToPointer(models.AclConfiguration1{
                    S3AclOption:           models.S3AclOption1_BucketOwnerFullControl,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:    map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            ResultReuseConfiguration: models.ToPointer(models.ResultReuseConfiguration1{
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
            }),
            AdditionalProperties:     map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



