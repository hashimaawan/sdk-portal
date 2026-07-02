# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.

*This model accepts additional fields of type object.*


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExecutorId` | `string` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` |
| `ExecutorType` | [`ExecutorType2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/executor-type-2.md) | Optional | - |
| `StartDateTime` | `int?` | Optional | - |
| `TerminationDateTime` | `int?` | Optional | - |
| `ExecutorState` | [`ExecutorState3?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/executor-state-3.md) | Optional | - |
| `ExecutorSize` | `int?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ExecutorsSummary executorsSummary = new ExecutorsSummary
{
    ExecutorId = "ExecutorId8",
    ExecutorType = ExecutorType2.Worker,
    StartDateTime = 52,
    TerminationDateTime = 56,
    ExecutorState = ExecutorState3.Creating,
    ExecutorSize = 222,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



