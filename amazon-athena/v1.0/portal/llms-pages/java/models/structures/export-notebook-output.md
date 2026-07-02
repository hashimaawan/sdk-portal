# Export Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`ExportNotebookOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NotebookMetadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/notebook-metadata-1.md) | Optional | - | NotebookMetadata1 getNotebookMetadata() | setNotebookMetadata(NotebookMetadata1 notebookMetadata) |
| `Payload` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` | String getPayload() | setPayload(String payload) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.ExportNotebookOutput;
import com.amazonaws.useast1.athena.models.NotebookMetadata1;
import com.amazonaws.useast1.athena.models.NotebookType1;
import java.io.IOException;

ExportNotebookOutput exportNotebookOutput = new ExportNotebookOutput.Builder()
    .notebookMetadata(new NotebookMetadata1.Builder()
        .notebookId("NotebookId0")
        .name("Name0")
        .workGroup("WorkGroup2")
        .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .type(NotebookType1.IPYNB)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .payload("Payload2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



