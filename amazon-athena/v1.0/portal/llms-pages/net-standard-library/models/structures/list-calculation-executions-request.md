# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `StateFilter` | [`CalculationExecutionState3?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/calculation-execution-state-3.md) | Optional | - |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ListCalculationExecutionsRequest listCalculationExecutionsRequest = new ListCalculationExecutionsRequest
{
    SessionId = "SessionId2",
    StateFilter = CalculationExecutionState3.Queued,
    MaxResults = 100,
    NextToken = "NextToken0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



