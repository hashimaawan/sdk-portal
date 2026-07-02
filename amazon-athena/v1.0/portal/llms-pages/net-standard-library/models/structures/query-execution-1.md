# Query Execution 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uMQ


# Class Name

`QueryExecution1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `Query` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `StatementType` | [`StatementType1Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/statement-type-1.md) | Optional | - |
| `ResultConfiguration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-configuration-1.md) | Optional | - |
| `ResultReuseConfiguration` | [`ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-reuse-configuration-1.md) | Optional | - |
| `QueryExecutionContext` | [`QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-execution-context-1.md) | Optional | - |
| `Status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/status.md) | Optional | - |
| `Statistics` | [`Statistics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/statistics.md) | Optional | - |
| `WorkGroup` | `string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/engine-version-1.md) | Optional | - |
| `ExecutionParameters` | `List<string>` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `SubstatementType` | `string` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

QueryExecution1 queryExecution1 = new QueryExecution1
{
    QueryExecutionId = "QueryExecutionId6",
    Query = "Query0",
    StatementType = StatementType1Enum.UTILITY,
    ResultConfiguration = new ResultConfiguration1
    {
        OutputLocation = "OutputLocation0",
        EncryptionConfiguration = new EncryptionConfiguration2
        {
            EncryptionOption = EncryptionOption1Enum.SSES3,
            KmsKey = "KmsKey6",
        },
        ExpectedBucketOwner = "ExpectedBucketOwner0",
        AclConfiguration = new AclConfiguration1
        {
            S3AclOption = S3AclOption1Enum.BUCKETOWNERFULLCONTROL,
        },
    },
    ResultReuseConfiguration = new ResultReuseConfiguration1
    {
        ResultReuseByAgeConfiguration = new ResultReuseByAgeConfiguration2
        {
            Enabled = false,
            MaxAgeInMinutes = 26,
        },
    },
};
```



