# Status 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXR1czM


# Class Name

`Status3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StartDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getStartDateTime() | setStartDateTime(LocalDateTime startDateTime) |
| `LastModifiedDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getLastModifiedDateTime() | setLastModifiedDateTime(LocalDateTime lastModifiedDateTime) |
| `EndDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getEndDateTime() | setEndDateTime(LocalDateTime endDateTime) |
| `IdleSinceDateTime` | `LocalDateTime` | Optional | - | LocalDateTime getIdleSinceDateTime() | setIdleSinceDateTime(LocalDateTime idleSinceDateTime) |
| `State` | [`SessionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/session-state-1.md) | Optional | - | SessionState1Enum getState() | setState(SessionState1Enum state) |
| `StateChangeReason` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getStateChangeReason() | setStateChangeReason(String stateChangeReason) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.SessionState1Enum;
import com.amazonaws.useast1.athena.models.Status3;

Status3 status3 = new Status3.Builder()
    .startDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .lastModifiedDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .endDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .idleSinceDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .state(SessionState1Enum.CREATING)
    .build();
```



