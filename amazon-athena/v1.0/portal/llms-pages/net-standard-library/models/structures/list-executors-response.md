# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ


# Class Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `NextToken` | `string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `ExecutorsSummary` | [`List<ExecutorsSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/executors-summary.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
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
            ExecutorType = ExecutorType2Enum.GATEWAY,
            StartDateTime = 128,
            TerminationDateTime = 236,
            ExecutorState = ExecutorState3Enum.TERMINATED,
            ExecutorSize = 42,
        },
        new ExecutorsSummary
        {
            ExecutorId = "ExecutorId8",
            ExecutorType = ExecutorType2Enum.GATEWAY,
            StartDateTime = 128,
            TerminationDateTime = 236,
            ExecutorState = ExecutorState3Enum.TERMINATED,
            ExecutorSize = 42,
        },
        new ExecutorsSummary
        {
            ExecutorId = "ExecutorId8",
            ExecutorType = ExecutorType2Enum.GATEWAY,
            StartDateTime = 128,
            TerminationDateTime = 236,
            ExecutorState = ExecutorState3Enum.TERMINATED,
            ExecutorSize = 42,
        },
    },
};
```



