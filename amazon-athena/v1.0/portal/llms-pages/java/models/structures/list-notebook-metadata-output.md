# List Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhT3V0cHV0


# Class Name

`ListNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `NotebookMetadataList` | [`List<NotebookMetadata>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/notebook-metadata.md) | Optional | - | List<NotebookMetadata> getNotebookMetadataList() | setNotebookMetadataList(List<NotebookMetadata> notebookMetadataList) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.ListNotebookMetadataOutput;
import com.amazonaws.useast1.athena.models.NotebookMetadata;
import com.amazonaws.useast1.athena.models.NotebookType1Enum;
import java.util.Arrays;

ListNotebookMetadataOutput listNotebookMetadataOutput = new ListNotebookMetadataOutput.Builder()
    .nextToken("NextToken2")
    .notebookMetadataList(Arrays.asList(
        new NotebookMetadata.Builder()
            .notebookId("NotebookId4")
            .name("Name4")
            .workGroup("WorkGroup6")
            .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .type(NotebookType1Enum.IPYNB)
            .build()
    ))
    .build();
```



