# Calculation Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdHVz

Contains information about the status of a notebook calculation.

*This model accepts additional fields of type object.*


# Class Name

`CalculationStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SubmissionDateTime` | `DateTime?` | Optional | - |
| `CompletionDateTime` | `DateTime?` | Optional | - |
| `State` | [`CalculationExecutionState1?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/calculation-execution-state-1.md) | Optional | - |
| `StateChangeReason` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Globalization;

CalculationStatus calculationStatus = new CalculationStatus
{
    SubmissionDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    CompletionDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    State = CalculationExecutionState1.Creating,
    StateChangeReason = "StateChangeReason2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



