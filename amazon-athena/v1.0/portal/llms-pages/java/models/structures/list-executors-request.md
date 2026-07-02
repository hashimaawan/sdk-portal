# List Executors Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ListExecutorsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `ExecutorStateFilter` | [`ExecutorState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/executor-state-1.md) | Optional | - | ExecutorState1 getExecutorStateFilter() | setExecutorStateFilter(ExecutorState1 executorStateFilter) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `NextToken` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ExecutorState1;
import com.amazonaws.useast1.athena.models.ListExecutorsRequest;
import java.io.IOException;

ListExecutorsRequest listExecutorsRequest = new ListExecutorsRequest.Builder(
    "SessionId0"
)
.executorStateFilter(ExecutorState1.CREATING)
.maxResults(100)
.nextToken("NextToken8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



