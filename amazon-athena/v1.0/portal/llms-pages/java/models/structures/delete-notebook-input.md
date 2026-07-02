# Delete Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRlbGV0ZU5vdGVib29rSW5wdXQ


# Class Name

`DeleteNotebookInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NotebookId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getNotebookId() | setNotebookId(String notebookId) |


# Example

```java
import com.amazonaws.useast1.athena.models.DeleteNotebookInput;

DeleteNotebookInput deleteNotebookInput = new DeleteNotebookInput.Builder(
    "NotebookId0"
)
.build();
```



