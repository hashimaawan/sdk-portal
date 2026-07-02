# Start Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25JbnB1dA


# Class Name

`StartQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `ClientRequestToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `QueryExecutionContext` | [`*models.QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-execution-context-1.md) | Optional | - |
| `ResultConfiguration` | [`*models.ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-configuration-1.md) | Optional | - |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `ExecutionParameters` | `[]string` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `ResultReuseConfiguration` | [`*models.ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-reuse-configuration-1.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    startQueryExecutionInput := models.StartQueryExecutionInput{
        QueryString:              "QueryString4",
        ClientRequestToken:       models.ToPointer("ClientRequestToken6"),
        QueryExecutionContext:    models.ToPointer(models.QueryExecutionContext1{
            Database:             models.ToPointer("Database4"),
            Catalog:              models.ToPointer("Catalog0"),
        }),
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
        WorkGroup:                models.ToPointer("WorkGroup4"),
        ExecutionParameters:      []string{
            "ExecutionParameters8",
        },
    }

}
```



