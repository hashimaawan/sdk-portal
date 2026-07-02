# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0


# Class Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `StateFilter` | [`CalculationExecutionState3Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/calculation-execution-state-3.md) | Optional | - |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `string` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```csharp
using AmazonAthena.Standard.Models;

ListCalculationExecutionsRequest listCalculationExecutionsRequest = new ListCalculationExecutionsRequest
{
    SessionId = "SessionId2",
    StateFilter = CalculationExecutionState3Enum.QUEUED,
    MaxResults = 100,
    NextToken = "NextToken0",
};
```



