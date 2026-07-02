# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXR1cw


# Class Name

`Status`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `State` | [`QueryExecutionState1Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/query-execution-state-1.md) | Optional | - |
| `StateChangeReason` | `string` | Optional | - |
| `SubmissionDateTime` | `DateTime?` | Optional | - |
| `CompletionDateTime` | `DateTime?` | Optional | - |
| `AthenaError` | [`AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/athena-error-2.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Globalization;

Status status = new Status
{
    State = QueryExecutionState1Enum.QUEUED,
    StateChangeReason = "StateChangeReason8",
    SubmissionDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    CompletionDateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    AthenaError = new AthenaError2
    {
        ErrorCategory = 3,
        ErrorType = 128,
        Retryable = false,
        ErrorMessage = "ErrorMessage8",
    },
};
```



