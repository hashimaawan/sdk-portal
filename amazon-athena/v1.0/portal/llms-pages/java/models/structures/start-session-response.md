# Start Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlc3BvbnNl


# Class Name

`StartSessionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `State` | [`SessionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/session-state-1.md) | Optional | - | SessionState1Enum getState() | setState(SessionState1Enum state) |


# Example

```java
import com.amazonaws.useast1.athena.models.SessionState1Enum;
import com.amazonaws.useast1.athena.models.StartSessionResponse;

StartSessionResponse startSessionResponse = new StartSessionResponse.Builder()
    .sessionId("SessionId4")
    .state(SessionState1Enum.CREATING)
    .build();
```



