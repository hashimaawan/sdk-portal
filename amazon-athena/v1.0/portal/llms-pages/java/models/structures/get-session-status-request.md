# Get Session Status Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFNlc3Npb25TdGF0dXNSZXF1ZXN0


# Class Name

`GetSessionStatusRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetSessionStatusRequest;

GetSessionStatusRequest getSessionStatusRequest = new GetSessionStatusRequest.Builder(
    "SessionId6"
)
.build();
```



