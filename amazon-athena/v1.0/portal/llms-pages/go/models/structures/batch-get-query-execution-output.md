# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutions` | [`[]models.QueryExecution`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-execution.md) | Optional | - |
| `UnprocessedQueryExecutionIds` | [`[]models.UnprocessedQueryExecutionId`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/unprocessed-query-execution-id.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    batchGetQueryExecutionOutput := models.BatchGetQueryExecutionOutput{
        QueryExecutions:              []models.QueryExecution{
            models.QueryExecution{
                QueryExecutionId:         models.ToPointer("QueryExecutionId6"),
                Query:                    models.ToPointer("Query0"),
                StatementType:            models.ToPointer(models.StatementType1_Utility),
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
            },
            models.QueryExecution{
                QueryExecutionId:         models.ToPointer("QueryExecutionId6"),
                Query:                    models.ToPointer("Query0"),
                StatementType:            models.ToPointer(models.StatementType1_Utility),
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
            },
        },
        UnprocessedQueryExecutionIds: []models.UnprocessedQueryExecutionId{
            models.UnprocessedQueryExecutionId{
                QueryExecutionId:      models.ToPointer("QueryExecutionId6"),
                ErrorCode:             models.ToPointer("ErrorCode2"),
                ErrorMessage:          models.ToPointer("ErrorMessage8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.UnprocessedQueryExecutionId{
                QueryExecutionId:      models.ToPointer("QueryExecutionId6"),
                ErrorCode:             models.ToPointer("ErrorCode2"),
                ErrorMessage:          models.ToPointer("ErrorMessage8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.UnprocessedQueryExecutionId{
                QueryExecutionId:      models.ToPointer("QueryExecutionId6"),
                ErrorCode:             models.ToPointer("ErrorCode2"),
                ErrorMessage:          models.ToPointer("ErrorMessage8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:         map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



