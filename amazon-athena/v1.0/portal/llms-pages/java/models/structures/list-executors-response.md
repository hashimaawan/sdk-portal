# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `NextToken` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` | String getNextToken() | setNextToken(String nextToken) |
| `ExecutorsSummary` | [`List<ExecutorsSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/executors-summary.md) | Optional | - | List<ExecutorsSummary> getExecutorsSummary() | setExecutorsSummary(List<ExecutorsSummary> executorsSummary) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ExecutorState3;
import com.amazonaws.useast1.athena.models.ExecutorType2;
import com.amazonaws.useast1.athena.models.ExecutorsSummary;
import com.amazonaws.useast1.athena.models.ListExecutorsResponse;
import java.io.IOException;
import java.util.Arrays;

ListExecutorsResponse listExecutorsResponse = new ListExecutorsResponse.Builder(
    "SessionId4"
)
.nextToken("NextToken4")
.executorsSummary(Arrays.asList(
        new ExecutorsSummary.Builder(
            "ExecutorId8"
        )
        .executorType(ExecutorType2.GATEWAY)
        .startDateTime(128)
        .terminationDateTime(236)
        .executorState(ExecutorState3.TERMINATED)
        .executorSize(42)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new ExecutorsSummary.Builder(
            "ExecutorId8"
        )
        .executorType(ExecutorType2.GATEWAY)
        .startDateTime(128)
        .terminationDateTime(236)
        .executorState(ExecutorState3.TERMINATED)
        .executorSize(42)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new ExecutorsSummary.Builder(
            "ExecutorId8"
        )
        .executorType(ExecutorType2.GATEWAY)
        .startDateTime(128)
        .terminationDateTime(236)
        .executorState(ExecutorState3.TERMINATED)
        .executorSize(42)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



