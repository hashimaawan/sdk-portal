# Notebook Metadata 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGEx

*This model accepts additional fields of type Object.*


# Class Name

`NotebookMetadata1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NotebookId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getNotebookId() | setNotebookId(String notebookId) |
| `Name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getName() | setName(String name) |
| `WorkGroup` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `CreationTime` | `LocalDateTime` | Optional | - | LocalDateTime getCreationTime() | setCreationTime(LocalDateTime creationTime) |
| `Type` | [`NotebookType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/notebook-type-1.md) | Optional | - | NotebookType1 getType() | setType(NotebookType1 type) |
| `LastModifiedTime` | `LocalDateTime` | Optional | - | LocalDateTime getLastModifiedTime() | setLastModifiedTime(LocalDateTime lastModifiedTime) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.NotebookMetadata1;
import com.amazonaws.useast1.athena.models.NotebookType1;
import java.io.IOException;

NotebookMetadata1 notebookMetadata1 = new NotebookMetadata1.Builder()
    .notebookId("NotebookId2")
    .name("Name2")
    .workGroup("WorkGroup4")
    .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .type(NotebookType1.IPYNB)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



