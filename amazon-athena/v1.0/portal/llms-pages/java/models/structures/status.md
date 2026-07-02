# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXR1cw

*This model accepts additional fields of type Object.*


# Class Name

`Status`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `State` | [`QueryExecutionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/query-execution-state-1.md) | Optional | - | QueryExecutionState1 getState() | setState(QueryExecutionState1 state) |
| `StateChangeReason` | `String` | Optional | - | String getStateChangeReason() | setStateChangeReason(String stateChangeReason) |
| `SubmissionDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getSubmissionDateTime() | setSubmissionDateTime(LocalDateTime submissionDateTime) |
| `CompletionDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getCompletionDateTime() | setCompletionDateTime(LocalDateTime completionDateTime) |
| `AthenaError` | [`AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/athena-error-2.md) | Optional | - | AthenaError2 getAthenaError() | setAthenaError(AthenaError2 athenaError) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.AthenaError2;
import com.amazonaws.useast1.athena.models.QueryExecutionState1;
import com.amazonaws.useast1.athena.models.Status;
import java.io.IOException;

Status status = new Status.Builder()
    .state(QueryExecutionState1.QUEUED)
    .stateChangeReason("StateChangeReason8")
    .submissionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .completionDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .athenaError(new AthenaError2.Builder()
        .errorCategory(3)
        .errorType(128)
        .retryable(false)
        .errorMessage("ErrorMessage8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



