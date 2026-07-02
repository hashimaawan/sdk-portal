# List Notebook Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`ListNotebookSessionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NotebookId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getNotebookId() | setNotebookId(String notebookId) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ListNotebookSessionsRequest;
import java.io.IOException;

ListNotebookSessionsRequest listNotebookSessionsRequest = new ListNotebookSessionsRequest.Builder(
    "NotebookId8"
)
.maxResults(14)
.nextToken("NextToken8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



