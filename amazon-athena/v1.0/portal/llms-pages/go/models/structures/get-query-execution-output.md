# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0


# Class Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecution` | [`*models.QueryExecution1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-execution-1.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getQueryExecutionOutput := models.GetQueryExecutionOutput{
        QueryExecution:       models.ToPointer(models.QueryExecution1{
            QueryExecutionId:         models.ToPointer("QueryExecutionId0"),
            Query:                    models.ToPointer("Query6"),
            StatementType:            models.ToPointer(models.StatementType1Enum_DDL),
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
        }),
    }

}
```



