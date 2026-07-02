# List Named Queries Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListNamedQueriesInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 50` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `WorkGroup` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ListNamedQueriesInput;
import java.io.IOException;

ListNamedQueriesInput listNamedQueriesInput = new ListNamedQueriesInput.Builder()
    .nextToken("NextToken8")
    .maxResults(50)
    .workGroup("WorkGroup0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



