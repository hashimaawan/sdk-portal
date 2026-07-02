# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q


# Class Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `StateFilter` | [`SessionState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/session-state-3.md) | Optional | - | SessionState3Enum getStateFilter() | setStateFilter(SessionState3Enum stateFilter) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `NextToken` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` | String getNextToken() | setNextToken(String nextToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.ListSessionsRequest;
import com.amazonaws.useast1.athena.models.SessionState3Enum;

ListSessionsRequest listSessionsRequest = new ListSessionsRequest.Builder(
    "WorkGroup8"
)
.stateFilter(SessionState3Enum.CREATING)
.maxResults(100)
.nextToken("NextToken6")
.build();
```



