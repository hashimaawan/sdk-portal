# Query Execution Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdHVz

The completion date, current state, submission time, and state change reason (if applicable) for the query execution.

*This model accepts additional fields of type object.*


# Class Name

`QueryExecutionStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `State` | [`QueryExecutionState1?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/query-execution-state-1.md) | Optional | - |
| `StateChangeReason` | `string` | Optional | - |
| `SubmissionDateTime` | `DateTime?` | Optional | - |
| `CompletionDateTime` | `DateTime?` | Optional | - |
| `AthenaError` | [`AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/athena-error-2.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Globalization;

QueryExecutionStatus queryExecutionStatus = new QueryExecutionStatus
{
    State = QueryExecutionState1.Succeeded,
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
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



