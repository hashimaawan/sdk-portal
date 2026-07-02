# Query Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2U

Stage statistics such as input and output rows and bytes, execution time and stage state. This information also includes substages and the query stage plan.


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


# Example

```csharp
using AmazonAthena.Standard.Models;

QueryStage queryStage = new QueryStage
{
    StageId = 118,
    State = "State0",
    OutputBytes = 120,
    OutputRows = 146,
    InputBytes = 178,
};
```



