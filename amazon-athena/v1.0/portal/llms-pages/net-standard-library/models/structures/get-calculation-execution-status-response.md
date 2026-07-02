# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U

*This model accepts additional fields of type object.*


# Class Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/status-1.md) | Optional | - |
| `Statistics` | [`Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/statistics-1.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Globalization;

GetCalculationExecutionStatusResponse getCalculationExecutionStatusResponse = new GetCalculationExecutionStatusResponse
{
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
    Statistics = new Statistics1
    {
        DpuExecutionInMillis = 164,
        Progress = "Progress6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



