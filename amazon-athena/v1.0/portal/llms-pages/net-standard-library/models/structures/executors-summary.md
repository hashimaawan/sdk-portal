# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExecutorId` | `string` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` |
| `ExecutorType` | [`ExecutorType2Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/executor-type-2.md) | Optional | - |
| `StartDateTime` | `int?` | Optional | - |
| `TerminationDateTime` | `int?` | Optional | - |
| `ExecutorState` | [`ExecutorState3Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/executor-state-3.md) | Optional | - |
| `ExecutorSize` | `int?` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

ExecutorsSummary executorsSummary = new ExecutorsSummary
{
    ExecutorId = "ExecutorId8",
    ExecutorType = ExecutorType2Enum.WORKER,
    StartDateTime = 52,
    TerminationDateTime = 56,
    ExecutorState = ExecutorState3Enum.CREATING,
    ExecutorSize = 222,
};
```



