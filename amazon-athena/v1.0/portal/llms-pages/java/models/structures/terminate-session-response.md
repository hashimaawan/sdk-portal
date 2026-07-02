# Terminate Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXNwb25zZQ


# Class Name

`TerminateSessionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `State` | [`SessionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/session-state-1.md) | Optional | - | SessionState1Enum getState() | setState(SessionState1Enum state) |


# Example

```java
import com.amazonaws.useast1.athena.models.SessionState1Enum;
import com.amazonaws.useast1.athena.models.TerminateSessionResponse;

TerminateSessionResponse terminateSessionResponse = new TerminateSessionResponse.Builder()
    .state(SessionState1Enum.CREATING)
    .build();
```



