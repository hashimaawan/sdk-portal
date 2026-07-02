# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXR1cw


# Class Name

`Status`


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
import com.amazonaws.useast1.athena.models.Status;

Status status = new Status.Builder()
    .state(QueryExecutionState1Enum.QUEUED)
    .stateChangeReason("StateChangeReason8")
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



