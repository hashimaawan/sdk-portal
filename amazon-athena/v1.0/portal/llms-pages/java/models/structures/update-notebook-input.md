# Update Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZU5vdGVib29rSW5wdXQ


# Class Name

`UpdateNotebookInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NotebookId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getNotebookId() | setNotebookId(String notebookId) |
| `Payload` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` | String getPayload() | setPayload(String payload) |
| `Type` | [`NotebookType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/notebook-type-2.md) | Required | - | NotebookType2Enum getType() | setType(NotebookType2Enum type) |
| `SessionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `ClientRequestToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getClientRequestToken() | setClientRequestToken(String clientRequestToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.NotebookType2Enum;
import com.amazonaws.useast1.athena.models.UpdateNotebookInput;

UpdateNotebookInput updateNotebookInput = new UpdateNotebookInput.Builder(
    "NotebookId8",
    "Payload4",
    NotebookType2Enum.IPYNB
)
.sessionId("SessionId0")
.clientRequestToken("ClientRequestToken2")
.build();
```



