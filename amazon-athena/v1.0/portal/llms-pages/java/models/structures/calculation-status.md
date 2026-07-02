# Calculation Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdHVz

Contains information about the status of a notebook calculation.

*This model accepts additional fields of type Object.*


# Class Name

`CalculationStatus`


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
import com.amazonaws.useast1.athena.models.CalculationStatus;
import java.io.IOException;

CalculationStatus calculationStatus = new CalculationStatus.Builder()
    .submissionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .completionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .state(CalculationExecutionState1.CREATING)
    .stateChangeReason("StateChangeReason2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



