# Query Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9u

Information about a single instance of a query execution.

*This model accepts additional fields of type interface{}.*


# Class Name

`QueryExecution`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `Query` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `StatementType` | [`*models.StatementType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/statement-type-1.md) | Optional | - |
| `ResultConfiguration` | [`*models.ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-configuration-1.md) | Optional | - |
| `ResultReuseConfiguration` | [`*models.ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-reuse-configuration-1.md) | Optional | - |
| `QueryExecutionContext` | [`*models.QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-execution-context-1.md) | Optional | - |
| `Status` | [`*models.Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/status.md) | Optional | - |
| `Statistics` | [`*models.Statistics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/statistics.md) | Optional | - |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `EngineVersion` | [`*models.EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/engine-version-1.md) | Optional | - |
| `ExecutionParameters` | `[]string` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `SubstatementType` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    queryExecution := models.QueryExecution{
        QueryExecutionId:         models.ToPointer("QueryExecutionId4"),
        Query:                    models.ToPointer("Query2"),
        StatementType:            models.ToPointer(models.StatementType1_Dml),
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
    }

}
```



