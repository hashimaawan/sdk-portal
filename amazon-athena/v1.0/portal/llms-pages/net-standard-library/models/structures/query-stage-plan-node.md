# Query Stage Plan Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFuTm9kZQ

Stage plan information such as name, identifier, sub plans, and remote sources.

*This model accepts additional fields of type object.*


# Class Name

`QueryStagePlanNode`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Optional | - |
| `Identifier` | `string` | Optional | - |
| `Children` | [`List<QueryStagePlanNode>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-stage-plan-node.md) | Optional | - |
| `RemoteSources` | `List<string>` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

QueryStagePlanNode queryStagePlanNode = new QueryStagePlanNode
{
    Name = "Name4",
    Identifier = "Identifier0",
    Children = new List<QueryStagePlanNode>
    {
        new QueryStagePlanNode
        {
            Name = "Name6",
            Identifier = "Identifier2",
            Children = new List<QueryStagePlanNode>
            {
                new QueryStagePlanNode
                {
                },
            },
            RemoteSources = new List<string>
            {
                "RemoteSources4",
                "RemoteSources5",
                "RemoteSources6",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    RemoteSources = new List<string>
    {
        "RemoteSources2",
        "RemoteSources3",
        "RemoteSources4",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



