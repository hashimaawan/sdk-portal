# Query Stage Plan

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFu


# Class Name

`QueryStagePlan`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Optional | - |
| `Identifier` | `string` | Optional | - |
| `Children` | [`List<QueryStagePlanNode>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-stage-plan-node.md) | Optional | - |
| `RemoteSources` | `List<string>` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

QueryStagePlan queryStagePlan = new QueryStagePlan
{
    Name = "Name0",
    Identifier = "Identifier6",
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
        },
    },
    RemoteSources = new List<string>
    {
        "RemoteSources8",
        "RemoteSources9",
        "RemoteSources0",
    },
};
```



