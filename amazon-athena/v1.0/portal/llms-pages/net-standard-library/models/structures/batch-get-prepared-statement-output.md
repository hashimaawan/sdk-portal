# Batch Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRPdXRwdXQ

*This model accepts additional fields of type object.*


# Class Name

`BatchGetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PreparedStatements` | [`List<PreparedStatement>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/prepared-statement.md) | Optional | - |
| `UnprocessedPreparedStatementNames` | [`List<UnprocessedPreparedStatementName>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/unprocessed-prepared-statement-name.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

BatchGetPreparedStatementOutput batchGetPreparedStatementOutput = new BatchGetPreparedStatementOutput
{
    PreparedStatements = new List<PreparedStatement>
    {
        new PreparedStatement
        {
            StatementName = "StatementName2",
            QueryStatement = "QueryStatement6",
            WorkGroupName = "WorkGroupName6",
            Description = "Description2",
            LastModifiedTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new PreparedStatement
        {
            StatementName = "StatementName2",
            QueryStatement = "QueryStatement6",
            WorkGroupName = "WorkGroupName6",
            Description = "Description2",
            LastModifiedTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    UnprocessedPreparedStatementNames = new List<UnprocessedPreparedStatementName>
    {
        new UnprocessedPreparedStatementName
        {
            StatementName = "StatementName0",
            ErrorCode = "ErrorCode2",
            ErrorMessage = "ErrorMessage8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new UnprocessedPreparedStatementName
        {
            StatementName = "StatementName0",
            ErrorCode = "ErrorCode2",
            ErrorMessage = "ErrorMessage8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new UnprocessedPreparedStatementName
        {
            StatementName = "StatementName0",
            ErrorCode = "ErrorCode2",
            ErrorMessage = "ErrorMessage8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



