# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutions` | [`List<QueryExecution>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-execution.md) | Optional | - |
| `UnprocessedQueryExecutionIds` | [`List<UnprocessedQueryExecutionId>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/unprocessed-query-execution-id.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

BatchGetQueryExecutionOutput batchGetQueryExecutionOutput = new BatchGetQueryExecutionOutput
{
    QueryExecutions = new List<QueryExecution>
    {
        new QueryExecution
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
        },
        new QueryExecution
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
        },
    },
    UnprocessedQueryExecutionIds = new List<UnprocessedQueryExecutionId>
    {
        new UnprocessedQueryExecutionId
        {
            QueryExecutionId = "QueryExecutionId6",
            ErrorCode = "ErrorCode2",
            ErrorMessage = "ErrorMessage8",
        },
        new UnprocessedQueryExecutionId
        {
            QueryExecutionId = "QueryExecutionId6",
            ErrorCode = "ErrorCode2",
            ErrorMessage = "ErrorMessage8",
        },
        new UnprocessedQueryExecutionId
        {
            QueryExecutionId = "QueryExecutionId6",
            ErrorCode = "ErrorCode2",
            ErrorMessage = "ErrorMessage8",
        },
    },
};
```



