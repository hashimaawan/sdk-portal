# List Notebook Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`ListNotebookSessionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NotebookSessionsList` | [`List<NotebookSessionSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/notebook-session-summary.md) | Required | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` | List<NotebookSessionSummary> getNotebookSessionsList() | setNotebookSessionsList(List<NotebookSessionSummary> notebookSessionsList) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.ListNotebookSessionsResponse;
import com.amazonaws.useast1.athena.models.NotebookSessionSummary;
import java.io.IOException;
import java.util.Arrays;

ListNotebookSessionsResponse listNotebookSessionsResponse = new ListNotebookSessionsResponse.Builder(
    Arrays.asList(
        new NotebookSessionSummary.Builder()
            .sessionId("SessionId4")
            .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
)
.nextToken("NextToken0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



