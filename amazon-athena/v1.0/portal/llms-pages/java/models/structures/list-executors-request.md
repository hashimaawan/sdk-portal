# List Executors Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXF1ZXN0


# Class Name

`ListExecutorsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `ExecutorStateFilter` | [`ExecutorState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/executor-state-1.md) | Optional | - | ExecutorState1Enum getExecutorStateFilter() | setExecutorStateFilter(ExecutorState1Enum executorStateFilter) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `NextToken` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` | String getNextToken() | setNextToken(String nextToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.ExecutorState1Enum;
import com.amazonaws.useast1.athena.models.ListExecutorsRequest;

ListExecutorsRequest listExecutorsRequest = new ListExecutorsRequest.Builder(
    "SessionId0"
)
.executorStateFilter(ExecutorState1Enum.CREATING)
.maxResults(100)
.nextToken("NextToken8")
.build();
```



