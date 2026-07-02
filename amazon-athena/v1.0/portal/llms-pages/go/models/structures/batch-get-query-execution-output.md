# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutions` | [`[]models.QueryExecution`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-execution.md) | Optional | - |
| `UnprocessedQueryExecutionIds` | [`[]models.UnprocessedQueryExecutionId`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/unprocessed-query-execution-id.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    batchGetQueryExecutionOutput := models.BatchGetQueryExecutionOutput{
        QueryExecutions:              []models.QueryExecution{
            models.QueryExecution{
                QueryExecutionId:         models.ToPointer("QueryExecutionId6"),
                Query:                    models.ToPointer("Query0"),
                StatementType:            models.ToPointer(models.StatementType1Enum_UTILITY),
                ResultConfiguration:      models.ToPointer(models.ResultConfiguration1{
                    OutputLocation:          models.ToPointer("OutputLocation0"),
                    EncryptionConfiguration: models.ToPointer(models.EncryptionConfiguration2{
                        EncryptionOption:     models.EncryptionOption1Enum_SSES3,
                        KmsKey:               models.ToPointer("KmsKey6"),
                    }),
                    ExpectedBucketOwner:     models.ToPointer("ExpectedBucketOwner0"),
                    AclConfiguration:        models.ToPointer(models.AclConfiguration1{
                        S3AclOption:          models.S3AclOption1Enum_BUCKETOWNERFULLCONTROL,
                    }),
                }),
                ResultReuseConfiguration: models.ToPointer(models.ResultReuseConfiguration1{
                    ResultReuseByAgeConfiguration: models.ToPointer(models.ResultReuseByAgeConfiguration2{
                        Enabled:              false,
                        MaxAgeInMinutes:      models.ToPointer(26),
                    }),
                }),
            },
            models.QueryExecution{
                QueryExecutionId:         models.ToPointer("QueryExecutionId6"),
                Query:                    models.ToPointer("Query0"),
                StatementType:            models.ToPointer(models.StatementType1Enum_UTILITY),
                ResultConfiguration:      models.ToPointer(models.ResultConfiguration1{
                    OutputLocation:          models.ToPointer("OutputLocation0"),
                    EncryptionConfiguration: models.ToPointer(models.EncryptionConfiguration2{
                        EncryptionOption:     models.EncryptionOption1Enum_SSES3,
                        KmsKey:               models.ToPointer("KmsKey6"),
                    }),
                    ExpectedBucketOwner:     models.ToPointer("ExpectedBucketOwner0"),
                    AclConfiguration:        models.ToPointer(models.AclConfiguration1{
                        S3AclOption:          models.S3AclOption1Enum_BUCKETOWNERFULLCONTROL,
                    }),
                }),
                ResultReuseConfiguration: models.ToPointer(models.ResultReuseConfiguration1{
                    ResultReuseByAgeConfiguration: models.ToPointer(models.ResultReuseByAgeConfiguration2{
                        Enabled:              false,
                        MaxAgeInMinutes:      models.ToPointer(26),
                    }),
                }),
            },
        },
        UnprocessedQueryExecutionIds: []models.UnprocessedQueryExecutionId{
            models.UnprocessedQueryExecutionId{
                QueryExecutionId:     models.ToPointer("QueryExecutionId6"),
                ErrorCode:            models.ToPointer("ErrorCode2"),
                ErrorMessage:         models.ToPointer("ErrorMessage8"),
            },
            models.UnprocessedQueryExecutionId{
                QueryExecutionId:     models.ToPointer("QueryExecutionId6"),
                ErrorCode:            models.ToPointer("ErrorCode2"),
                ErrorMessage:         models.ToPointer("ErrorMessage8"),
            },
            models.UnprocessedQueryExecutionId{
                QueryExecutionId:     models.ToPointer("QueryExecutionId6"),
                ErrorCode:            models.ToPointer("ErrorCode2"),
                ErrorMessage:         models.ToPointer("ErrorMessage8"),
            },
        },
    }

}
```



