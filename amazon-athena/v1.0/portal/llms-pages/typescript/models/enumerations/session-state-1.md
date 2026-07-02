# Session State 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0ZTE

<p>The state of the session. A description of each state follows.</p> <p> <code>CREATING</code> - The session is being started, including acquiring resources.</p> <p> <code>CREATED</code> - The session has been started.</p> <p> <code>IDLE</code> - The session is able to accept a calculation.</p> <p> <code>BUSY</code> - The session is processing another task and is unable to accept a calculation.</p> <p> <code>TERMINATING</code> - The session is in the process of shutting down.</p> <p> <code>TERMINATED</code> - The session and its resources are no longer running.</p> <p> <code>DEGRADED</code> - The session has no healthy coordinators.</p> <p> <code>FAILED</code> - Due to a failure, the session and its resources are no longer running.</p>



# Enum Type Name

`SessionState1Enum`


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

```ts
import { SessionState1Enum } from 'amazon-athenalib';

const sessionState1 = SessionState1Enum.DEGRADED;
```



