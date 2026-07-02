# List Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Filters` | [`Filters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/filters.md) | Optional | - | Filters getFilters() | setFilters(Filters filters) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 50` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.Filters;
import com.amazonaws.useast1.athena.models.ListNotebookMetadataInput;
import java.io.IOException;

ListNotebookMetadataInput listNotebookMetadataInput = new ListNotebookMetadataInput.Builder(
    "WorkGroup4"
)
.filters(new Filters.Builder()
        .name("Name2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.nextToken("NextToken2")
.maxResults(50)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



