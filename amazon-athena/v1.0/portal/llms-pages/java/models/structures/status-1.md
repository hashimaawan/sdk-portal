# Status 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXR1czE


# Class Name

`Status1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SubmissionDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getSubmissionDateTime() | setSubmissionDateTime(LocalDateTime submissionDateTime) |
| `CompletionDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getCompletionDateTime() | setCompletionDateTime(LocalDateTime completionDateTime) |
| `State` | [`CalculationExecutionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/calculation-execution-state-1.md) | Optional | - | CalculationExecutionState1Enum getState() | setState(CalculationExecutionState1Enum state) |
| `StateChangeReason` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getStateChangeReason() | setStateChangeReason(String stateChangeReason) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.CalculationExecutionState1Enum;
import com.amazonaws.useast1.athena.models.Status1;

Status1 status1 = new Status1.Builder()
    .submissionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .completionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .state(CalculationExecutionState1Enum.QUEUED)
    .stateChangeReason("StateChangeReason0")
    .build();
```



