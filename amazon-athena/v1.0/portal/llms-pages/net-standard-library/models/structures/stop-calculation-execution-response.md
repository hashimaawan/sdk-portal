# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl


# Class Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `State` | [`CalculationExecutionState4Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/calculation-execution-state-4.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

StopCalculationExecutionResponse stopCalculationExecutionResponse = new StopCalculationExecutionResponse
{
    State = CalculationExecutionState4Enum.QUEUED,
};
```



