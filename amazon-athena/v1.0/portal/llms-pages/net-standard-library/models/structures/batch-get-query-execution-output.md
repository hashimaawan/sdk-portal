# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type object.*


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutions` | [`List<QueryExecution>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-execution.md) | Optional | - |
| `UnprocessedQueryExecutionIds` | [`List<UnprocessedQueryExecutionId>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/unprocessed-query-execution-id.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

BatchGetQueryExecutionOutput batchGetQueryExecutionOutput = new BatchGetQueryExecutionOutput
{
    QueryExecutions = new List<QueryExecution>
    {
        new QueryExecution
        {
            QueryExecutionId = "QueryExecutionId6",
            Query = "Query0",
            StatementType = StatementType1.Utility,
            ResultConfiguration = new ResultConfiguration1
            {
                OutputLocation = "OutputLocation0",
                EncryptionConfiguration = new EncryptionConfiguration2
                {
                    EncryptionOption = EncryptionOption1.SseS3,
                    KmsKey = "KmsKey6",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ExpectedBucketOwner = "ExpectedBucketOwner0",
                AclConfiguration = new AclConfiguration1
                {
                    S3AclOption = S3AclOption1.BucketOwnerFullControl,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ResultReuseConfiguration = new ResultReuseConfiguration1
            {
                ResultReuseByAgeConfiguration = new ResultReuseByAgeConfiguration2
                {
                    Enabled = false,
                    MaxAgeInMinutes = 26,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new QueryExecution
        {
            QueryExecutionId = "QueryExecutionId6",
            Query = "Query0",
            StatementType = StatementType1.Utility,
            ResultConfiguration = new ResultConfiguration1
            {
                OutputLocation = "OutputLocation0",
                EncryptionConfiguration = new EncryptionConfiguration2
                {
                    EncryptionOption = EncryptionOption1.SseS3,
                    KmsKey = "KmsKey6",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ExpectedBucketOwner = "ExpectedBucketOwner0",
                AclConfiguration = new AclConfiguration1
                {
                    S3AclOption = S3AclOption1.BucketOwnerFullControl,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ResultReuseConfiguration = new ResultReuseConfiguration1
            {
                ResultReuseByAgeConfiguration = new ResultReuseByAgeConfiguration2
                {
                    Enabled = false,
                    MaxAgeInMinutes = 26,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    UnprocessedQueryExecutionIds = new List<UnprocessedQueryExecutionId>
    {
        new UnprocessedQueryExecutionId
        {
            QueryExecutionId = "QueryExecutionId6",
            ErrorCode = "ErrorCode2",
            ErrorMessage = "ErrorMessage8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new UnprocessedQueryExecutionId
        {
            QueryExecutionId = "QueryExecutionId6",
            ErrorCode = "ErrorCode2",
            ErrorMessage = "ErrorMessage8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new UnprocessedQueryExecutionId
        {
            QueryExecutionId = "QueryExecutionId6",
            ErrorCode = "ErrorCode2",
            ErrorMessage = "ErrorMessage8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



