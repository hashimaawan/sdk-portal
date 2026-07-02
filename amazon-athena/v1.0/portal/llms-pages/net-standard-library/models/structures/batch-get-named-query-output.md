# Batch Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeU91dHB1dA

*This model accepts additional fields of type object.*


# Class Name

`BatchGetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueries` | [`List<NamedQuery>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/named-query.md) | Optional | - |
| `UnprocessedNamedQueryIds` | [`List<UnprocessedNamedQueryId>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/unprocessed-named-query-id.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

BatchGetNamedQueryOutput batchGetNamedQueryOutput = new BatchGetNamedQueryOutput
{
    NamedQueries = new List<NamedQuery>
    {
        new NamedQuery
        {
            Name = "Name2",
            Database = "Database0",
            QueryString = "QueryString4",
            Description = "Description4",
            NamedQueryId = "NamedQueryId0",
            WorkGroup = "WorkGroup4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new NamedQuery
        {
            Name = "Name2",
            Database = "Database0",
            QueryString = "QueryString4",
            Description = "Description4",
            NamedQueryId = "NamedQueryId0",
            WorkGroup = "WorkGroup4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new NamedQuery
        {
            Name = "Name2",
            Database = "Database0",
            QueryString = "QueryString4",
            Description = "Description4",
            NamedQueryId = "NamedQueryId0",
            WorkGroup = "WorkGroup4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    UnprocessedNamedQueryIds = new List<UnprocessedNamedQueryId>
    {
        new UnprocessedNamedQueryId
        {
            NamedQueryId = "NamedQueryId4",
            ErrorCode = "ErrorCode6",
            ErrorMessage = "ErrorMessage4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new UnprocessedNamedQueryId
        {
            NamedQueryId = "NamedQueryId4",
            ErrorCode = "ErrorCode6",
            ErrorMessage = "ErrorMessage4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



