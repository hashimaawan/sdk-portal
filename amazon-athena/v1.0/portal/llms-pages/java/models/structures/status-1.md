# Status 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXR1czE

*This model accepts additional fields of type Object.*


# Class Name

`Status1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SubmissionDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getSubmissionDateTime() | setSubmissionDateTime(LocalDateTime submissionDateTime) |
| `CompletionDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getCompletionDateTime() | setCompletionDateTime(LocalDateTime completionDateTime) |
| `State` | [`CalculationExecutionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/calculation-execution-state-1.md) | Optional | - | CalculationExecutionState1 getState() | setState(CalculationExecutionState1 state) |
| `StateChangeReason` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getStateChangeReason() | setStateChangeReason(String stateChangeReason) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.CalculationExecutionState1;
import com.amazonaws.useast1.athena.models.Status1;
import java.io.IOException;

Status1 status1 = new Status1.Builder()
    .submissionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .completionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .state(CalculationExecutionState1.QUEUED)
    .stateChangeReason("StateChangeReason0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



