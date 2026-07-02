# Start Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`StartSessionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `State` | [`SessionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/session-state-1.md) | Optional | - | SessionState1 getState() | setState(SessionState1 state) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.SessionState1;
import com.amazonaws.useast1.athena.models.StartSessionResponse;
import java.io.IOException;

StartSessionResponse startSessionResponse = new StartSessionResponse.Builder()
    .sessionId("SessionId4")
    .state(SessionState1.CREATING)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



