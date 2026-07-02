# Query Execution Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdHVz

The completion date, current state, submission time, and state change reason (if applicable) for the query execution.


# Class Name

`QueryExecutionStatus`


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

QueryExecutionStatus queryExecutionStatus = new QueryExecutionStatus
{
    State = QueryExecutionState1Enum.SUCCEEDED,
    StateChangeReason = "StateChangeReason0",
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



