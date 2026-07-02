# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.

*This model accepts additional fields of type Object.*


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExecutorId` | `String` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` | String getExecutorId() | setExecutorId(String executorId) |
| `ExecutorType` | [`ExecutorType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/executor-type-2.md) | Optional | - | ExecutorType2 getExecutorType() | setExecutorType(ExecutorType2 executorType) |
| `StartDateTime` | `Integer` | Optional | - | Integer getStartDateTime() | setStartDateTime(Integer startDateTime) |
| `TerminationDateTime` | `Integer` | Optional | - | Integer getTerminationDateTime() | setTerminationDateTime(Integer terminationDateTime) |
| `ExecutorState` | [`ExecutorState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/executor-state-3.md) | Optional | - | ExecutorState3 getExecutorState() | setExecutorState(ExecutorState3 executorState) |
| `ExecutorSize` | `Integer` | Optional | - | Integer getExecutorSize() | setExecutorSize(Integer executorSize) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.ExecutorState3;
import com.amazonaws.useast1.athena.models.ExecutorType2;
import com.amazonaws.useast1.athena.models.ExecutorsSummary;
import java.io.IOException;

ExecutorsSummary executorsSummary = new ExecutorsSummary.Builder(
    "ExecutorId8"
)
.executorType(ExecutorType2.WORKER)
.startDateTime(52)
.terminationDateTime(56)
.executorState(ExecutorState3.CREATING)
.executorSize(222)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



