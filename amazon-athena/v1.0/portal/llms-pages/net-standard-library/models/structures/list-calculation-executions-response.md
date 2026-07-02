# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ

*This model accepts additional fields of type object.*


# Class Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `Calculations` | [`List<CalculationSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

ListCalculationExecutionsResponse listCalculationExecutionsResponse = new ListCalculationExecutionsResponse
{
    NextToken = "NextToken8",
    Calculations = new List<CalculationSummary>
    {
        new CalculationSummary
        {
            CalculationExecutionId = "CalculationExecutionId0",
            Description = "Description2",
            Status = new Status1
            {
                SubmissionDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                CompletionDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                    provider: CultureInfo.InvariantCulture,
                    DateTimeStyles.RoundtripKind),
                State = CalculationExecutionState1.Canceling,
                StateChangeReason = "StateChangeReason8",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



