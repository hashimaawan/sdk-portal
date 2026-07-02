# Query Execution 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uMQ


# Class Name

`QueryExecution1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `Query` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `StatementType` | [`*models.StatementType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/statement-type-1.md) | Optional | - |
| `ResultConfiguration` | [`*models.ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-configuration-1.md) | Optional | - |
| `ResultReuseConfiguration` | [`*models.ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-reuse-configuration-1.md) | Optional | - |
| `QueryExecutionContext` | [`*models.QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-execution-context-1.md) | Optional | - |
| `Status` | [`*models.Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/status.md) | Optional | - |
| `Statistics` | [`*models.Statistics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/statistics.md) | Optional | - |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `EngineVersion` | [`*models.EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/engine-version-1.md) | Optional | - |
| `ExecutionParameters` | `[]string` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `SubstatementType` | `*string` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    queryExecution1 := models.QueryExecution1{
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
    }

}
```



