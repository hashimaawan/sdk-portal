# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ

*This model accepts additional fields of type object.*


# Class Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `NextToken` | `string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `ExecutorsSummary` | [`List<ExecutorsSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/executors-summary.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

ListExecutorsResponse listExecutorsResponse = new ListExecutorsResponse
{
    SessionId = "SessionId4",
    NextToken = "NextToken4",
    ExecutorsSummary = new List<ExecutorsSummary>
    {
        new ExecutorsSummary
        {
            ExecutorId = "ExecutorId8",
            ExecutorType = ExecutorType2.Gateway,
            StartDateTime = 128,
            TerminationDateTime = 236,
            ExecutorState = ExecutorState3.Terminated,
            ExecutorSize = 42,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ExecutorsSummary
        {
            ExecutorId = "ExecutorId8",
            ExecutorType = ExecutorType2.Gateway,
            StartDateTime = 128,
            TerminationDateTime = 236,
            ExecutorState = ExecutorState3.Terminated,
            ExecutorSize = 42,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ExecutorsSummary
        {
            ExecutorId = "ExecutorId8",
            ExecutorType = ExecutorType2.Gateway,
            StartDateTime = 128,
            TerminationDateTime = 236,
            ExecutorState = ExecutorState3.Terminated,
            ExecutorSize = 42,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



