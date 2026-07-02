# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `StateFilter` | [`SessionState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/session-state-3.md) | Optional | - | SessionState3 getStateFilter() | setStateFilter(SessionState3 stateFilter) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `NextToken` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ListSessionsRequest;
import com.amazonaws.useast1.athena.models.SessionState3;
import java.io.IOException;

ListSessionsRequest listSessionsRequest = new ListSessionsRequest.Builder(
    "WorkGroup8"
)
.stateFilter(SessionState3.CREATING)
.maxResults(100)
.nextToken("NextToken6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



