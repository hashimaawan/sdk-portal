# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ


# Class Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CalculationExecutionId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `State` | [`CalculationExecutionState4Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/calculation-execution-state-4.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

StartCalculationExecutionResponse startCalculationExecutionResponse = new StartCalculationExecutionResponse
{
    CalculationExecutionId = "CalculationExecutionId0",
    State = CalculationExecutionState4Enum.CANCELING,
};
```



