# Session State 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0ZTM

<p>A filter for a specific session state. A description of each state follows.</p> <p> <code>CREATING</code> - The session is being started, including acquiring resources.</p> <p> <code>CREATED</code> - The session has been started.</p> <p> <code>IDLE</code> - The session is able to accept a calculation.</p> <p> <code>BUSY</code> - The session is processing another task and is unable to accept a calculation.</p> <p> <code>TERMINATING</code> - The session is in the process of shutting down.</p> <p> <code>TERMINATED</code> - The session and its resources are no longer running.</p> <p> <code>DEGRADED</code> - The session has no healthy coordinators.</p> <p> <code>FAILED</code> - Due to a failure, the session and its resources are no longer running.</p>



# Enum Type Name

`SessionState3Enum`


# Fields

| Name |
|  --- |
| `CREATING` |
| `CREATED` |
| `IDLE` |
| `BUSY` |
| `TERMINATING` |
| `TERMINATED` |
| `DEGRADED` |
| `FAILED` |


# Example

```java
import com.amazonaws.useast1.athena.models.SessionState3Enum;

SessionState3Enum sessionState3 = SessionState3Enum.DEGRADED;
```



