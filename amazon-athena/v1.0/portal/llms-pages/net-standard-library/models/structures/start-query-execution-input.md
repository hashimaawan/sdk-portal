# Start Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25JbnB1dA

*This model accepts additional fields of type object.*


# Class Name

`StartQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `ClientRequestToken` | `string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `QueryExecutionContext` | [`QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-execution-context-1.md) | Optional | - |
| `ResultConfiguration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-configuration-1.md) | Optional | - |
| `WorkGroup` | `string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `ExecutionParameters` | `List<string>` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `ResultReuseConfiguration` | [`ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-reuse-configuration-1.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

StartQueryExecutionInput startQueryExecutionInput = new StartQueryExecutionInput
{
    QueryString = "QueryString4",
    ClientRequestToken = "ClientRequestToken6",
    QueryExecutionContext = new QueryExecutionContext1
    {
        Database = "Database4",
        Catalog = "Catalog0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
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
    WorkGroup = "WorkGroup4",
    ExecutionParameters = new List<string>
    {
        "ExecutionParameters8",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



