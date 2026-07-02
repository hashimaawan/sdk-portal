# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `StateFilter` | [`CalculationExecutionState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/calculation-execution-state-3.md) | Optional | - | CalculationExecutionState3 getStateFilter() | setStateFilter(CalculationExecutionState3 stateFilter) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` | Integer getMaxResults() | setMaxResults(Integer maxResults) |
| `NextToken` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CalculationExecutionState3;
import com.amazonaws.useast1.athena.models.ListCalculationExecutionsRequest;
import java.io.IOException;

ListCalculationExecutionsRequest listCalculationExecutionsRequest = new ListCalculationExecutionsRequest.Builder(
    "SessionId2"
)
.stateFilter(CalculationExecutionState3.QUEUED)
.maxResults(100)
.nextToken("NextToken0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



