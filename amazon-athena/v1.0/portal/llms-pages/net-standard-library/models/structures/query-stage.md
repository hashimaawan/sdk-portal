# Query Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2U

Stage statistics such as input and output rows and bytes, execution time and stage state. This information also includes substages and the query stage plan.

*This model accepts additional fields of type object.*


# Class Name

`QueryStage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StageId` | `int?` | Optional | - |
| `State` | `string` | Optional | - |
| `OutputBytes` | `int?` | Optional | - |
| `OutputRows` | `int?` | Optional | - |
| `InputBytes` | `int?` | Optional | - |
| `InputRows` | `int?` | Optional | - |
| `ExecutionTime` | `int?` | Optional | - |
| `QueryStagePlan` | [`QueryStagePlan`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-stage-plan.md) | Optional | - |
| `SubStages` | [`List<QueryStage>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-stage.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

QueryStage queryStage = new QueryStage
{
    StageId = 118,
    State = "State0",
    OutputBytes = 120,
    OutputRows = 146,
    InputBytes = 178,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



