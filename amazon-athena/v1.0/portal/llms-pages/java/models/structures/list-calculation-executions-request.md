# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0


# Class Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `StateFilter` | [`CalculationExecutionState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/calculation-execution-state-3.md) | Optional | - | CalculationExecutionState3Enum getStateFilter() | setStateFilter(CalculationExecutionState3Enum stateFilter) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `NextToken` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` | String getNextToken() | setNextToken(String nextToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.CalculationExecutionState3Enum;
import com.amazonaws.useast1.athena.models.ListCalculationExecutionsRequest;

ListCalculationExecutionsRequest listCalculationExecutionsRequest = new ListCalculationExecutionsRequest.Builder(
    "SessionId2"
)
.stateFilter(CalculationExecutionState3Enum.QUEUED)
.maxResults(100)
.nextToken("NextToken0")
.build();
```



