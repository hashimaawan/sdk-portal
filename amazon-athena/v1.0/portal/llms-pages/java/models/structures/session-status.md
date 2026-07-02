# Session Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0dXM

Contains information about the status of a session.

*This model accepts additional fields of type Object.*


# Class Name

`SessionStatus`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StartDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getStartDateTime() | setStartDateTime(LocalDateTime startDateTime) |
| `LastModifiedDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getLastModifiedDateTime() | setLastModifiedDateTime(LocalDateTime lastModifiedDateTime) |
| `EndDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getEndDateTime() | setEndDateTime(LocalDateTime endDateTime) |
| `IdleSinceDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getIdleSinceDateTime() | setIdleSinceDateTime(LocalDateTime idleSinceDateTime) |
| `State` | [`SessionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/session-state-1.md) | Optional | - | SessionState1 getState() | setState(SessionState1 state) |
| `StateChangeReason` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getStateChangeReason() | setStateChangeReason(String stateChangeReason) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.SessionState1;
import com.amazonaws.useast1.athena.models.SessionStatus;
import java.io.IOException;

SessionStatus sessionStatus = new SessionStatus.Builder()
    .startDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .lastModifiedDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .endDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .idleSinceDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .state(SessionState1.IDLE)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



