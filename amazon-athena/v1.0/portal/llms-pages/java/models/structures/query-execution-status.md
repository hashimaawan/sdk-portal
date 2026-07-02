# Query Execution Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdHVz

The completion date, current state, submission time, and state change reason (if applicable) for the query execution.


# Class Name

`QueryExecutionStatus`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `State` | [`QueryExecutionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/query-execution-state-1.md) | Optional | - | QueryExecutionState1Enum getState() | setState(QueryExecutionState1Enum state) |
| `StateChangeReason` | `String` | Optional | - | String getStateChangeReason() | setStateChangeReason(String stateChangeReason) |
| `SubmissionDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getSubmissionDateTime() | setSubmissionDateTime(LocalDateTime submissionDateTime) |
| `CompletionDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getCompletionDateTime() | setCompletionDateTime(LocalDateTime completionDateTime) |
| `AthenaError` | [`AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/athena-error-2.md) | Optional | - | AthenaError2 getAthenaError() | setAthenaError(AthenaError2 athenaError) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.AthenaError2;
import com.amazonaws.useast1.athena.models.QueryExecutionState1Enum;
import com.amazonaws.useast1.athena.models.QueryExecutionStatus;

QueryExecutionStatus queryExecutionStatus = new QueryExecutionStatus.Builder()
    .state(QueryExecutionState1Enum.SUCCEEDED)
    .stateChangeReason("StateChangeReason0")
    .submissionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .completionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .athenaError(new AthenaError2.Builder()
        .errorCategory(3)
        .errorType(128)
        .retryable(false)
        .errorMessage("ErrorMessage8")
        .build())
    .build();
```



