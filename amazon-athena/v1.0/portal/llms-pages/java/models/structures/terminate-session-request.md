# Terminate Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXF1ZXN0


# Class Name

`TerminateSessionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |


# Example

```java
import com.amazonaws.useast1.athena.models.TerminateSessionRequest;

TerminateSessionRequest terminateSessionRequest = new TerminateSessionRequest.Builder(
    "SessionId0"
)
.build();
```



