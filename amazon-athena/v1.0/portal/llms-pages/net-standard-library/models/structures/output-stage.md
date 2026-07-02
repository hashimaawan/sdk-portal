# Output Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk91dHB1dFN0YWdl


# Class Name

`OutputStage`


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

OutputStage outputStage = new OutputStage
{
    StageId = 26,
    State = "State4",
    OutputBytes = 212,
    OutputRows = 54,
    InputBytes = 170,
};
```



