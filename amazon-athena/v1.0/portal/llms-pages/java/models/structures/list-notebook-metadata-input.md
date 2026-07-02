# List Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhSW5wdXQ


# Class Name

`ListNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Filters` | [`Filters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/filters.md) | Optional | - | Filters getFilters() | setFilters(Filters filters) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 50` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |


# Example

```java
import com.amazonaws.useast1.athena.models.Filters;
import com.amazonaws.useast1.athena.models.ListNotebookMetadataInput;

ListNotebookMetadataInput listNotebookMetadataInput = new ListNotebookMetadataInput.Builder(
    "WorkGroup4"
)
.filters(new Filters.Builder()
        .name("Name2")
        .build())
.nextToken("NextToken2")
.maxResults(50)
.build();
```



