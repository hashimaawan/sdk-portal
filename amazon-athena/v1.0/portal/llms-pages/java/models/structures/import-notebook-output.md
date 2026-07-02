# Import Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkltcG9ydE5vdGVib29rT3V0cHV0


# Class Name

`ImportNotebookOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NotebookId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getNotebookId() | setNotebookId(String notebookId) |


# Example

```java
import com.amazonaws.useast1.athena.models.ImportNotebookOutput;

ImportNotebookOutput importNotebookOutput = new ImportNotebookOutput.Builder()
    .notebookId("NotebookId2")
    .build();
```



