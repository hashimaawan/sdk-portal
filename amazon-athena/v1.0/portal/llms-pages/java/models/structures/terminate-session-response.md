# Terminate Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`TerminateSessionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `State` | [`SessionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/session-state-1.md) | Optional | - | SessionState1 getState() | setState(SessionState1 state) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.SessionState1;
import com.amazonaws.useast1.athena.models.TerminateSessionResponse;
import java.io.IOException;

TerminateSessionResponse terminateSessionResponse = new TerminateSessionResponse.Builder()
    .state(SessionState1.CREATING)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



