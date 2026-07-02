# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ

*This model accepts additional fields of type object.*


# Class Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CalculationExecutionId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `State` | [`CalculationExecutionState4?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/calculation-execution-state-4.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

StartCalculationExecutionResponse startCalculationExecutionResponse = new StartCalculationExecutionResponse
{
    CalculationExecutionId = "CalculationExecutionId0",
    State = CalculationExecutionState4.Canceling,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



