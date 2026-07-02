# Import Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkltcG9ydE5vdGVib29rSW5wdXQ


# Class Name

`ImportNotebookInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getName() | setName(String name) |
| `Payload` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` | String getPayload() | setPayload(String payload) |
| `Type` | [`NotebookType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/notebook-type-2.md) | Required | - | NotebookType2Enum getType() | setType(NotebookType2Enum type) |
| `ClientRequestToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getClientRequestToken() | setClientRequestToken(String clientRequestToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.ImportNotebookInput;
import com.amazonaws.useast1.athena.models.NotebookType2Enum;

ImportNotebookInput importNotebookInput = new ImportNotebookInput.Builder(
    "WorkGroup2",
    "Name0",
    "Payload6",
    NotebookType2Enum.IPYNB
)
.clientRequestToken("ClientRequestToken4")
.build();
```



