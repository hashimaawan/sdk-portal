# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExecutorId` | `String` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` | String getExecutorId() | setExecutorId(String executorId) |
| `ExecutorType` | [`ExecutorType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/executor-type-2.md) | Optional | - | ExecutorType2Enum getExecutorType() | setExecutorType(ExecutorType2Enum executorType) |
| `StartDateTime` | `Integer` | Optional | - | Integer getStartDateTime() | setStartDateTime(Integer startDateTime) |
| `TerminationDateTime` | `Integer` | Optional | - | Integer getTerminationDateTime() | setTerminationDateTime(Integer terminationDateTime) |
| `ExecutorState` | [`ExecutorState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/executor-state-3.md) | Optional | - | ExecutorState3Enum getExecutorState() | setExecutorState(ExecutorState3Enum executorState) |
| `ExecutorSize` | `Integer` | Optional | - | Integer getExecutorSize() | setExecutorSize(Integer executorSize) |


# Example

```java
import com.amazonaws.useast1.athena.models.ExecutorState3Enum;
import com.amazonaws.useast1.athena.models.ExecutorType2Enum;
import com.amazonaws.useast1.athena.models.ExecutorsSummary;

ExecutorsSummary executorsSummary = new ExecutorsSummary.Builder(
    "ExecutorId8"
)
.executorType(ExecutorType2Enum.WORKER)
.startDateTime(52)
.terminationDateTime(56)
.executorState(ExecutorState3Enum.CREATING)
.executorSize(222)
.build();
```



