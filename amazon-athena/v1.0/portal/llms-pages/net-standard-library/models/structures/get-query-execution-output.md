# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0


# Class Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecution` | [`QueryExecution1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-execution-1.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

GetQueryExecutionOutput getQueryExecutionOutput = new GetQueryExecutionOutput
{
    QueryExecution = new QueryExecution1
    {
        QueryExecutionId = "QueryExecutionId0",
        Query = "Query6",
        StatementType = StatementType1Enum.DDL,
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
    },
};
```



