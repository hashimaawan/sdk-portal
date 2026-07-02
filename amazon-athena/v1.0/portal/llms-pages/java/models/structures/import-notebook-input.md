# Import Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkltcG9ydE5vdGVib29rSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ImportNotebookInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getName() | setName(String name) |
| `Payload` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` | String getPayload() | setPayload(String payload) |
| `Type` | [`NotebookType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/notebook-type-2.md) | Required | - | NotebookType2 getType() | setType(NotebookType2 type) |
| `ClientRequestToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getClientRequestToken() | setClientRequestToken(String clientRequestToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ImportNotebookInput;
import com.amazonaws.useast1.athena.models.NotebookType2;
import java.io.IOException;

ImportNotebookInput importNotebookInput = new ImportNotebookInput.Builder(
    "WorkGroup2",
    "Name0",
    "Payload6",
    NotebookType2.IPYNB
)
.clientRequestToken("ClientRequestToken4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



