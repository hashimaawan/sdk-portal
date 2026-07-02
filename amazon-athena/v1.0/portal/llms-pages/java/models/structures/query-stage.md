# Query Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2U

Stage statistics such as input and output rows and bytes, execution time and stage state. This information also includes substages and the query stage plan.

*This model accepts additional fields of type Object.*


# Class Name

`QueryStage`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StageId` | `Integer` | Optional | - | Integer getStageId() | setStageId(Integer stageId) |
| `State` | `String` | Optional | - | String getState() | setState(String state) |
| `OutputBytes` | `Integer` | Optional | - | Integer getOutputBytes() | setOutputBytes(Integer outputBytes) |
| `OutputRows` | `Integer` | Optional | - | Integer getOutputRows() | setOutputRows(Integer outputRows) |
| `InputBytes` | `Integer` | Optional | - | Integer getInputBytes() | setInputBytes(Integer inputBytes) |
| `InputRows` | `Integer` | Optional | - | Integer getInputRows() | setInputRows(Integer inputRows) |
| `ExecutionTime` | `Integer` | Optional | - | Integer getExecutionTime() | setExecutionTime(Integer executionTime) |
| `QueryStagePlan` | [`QueryStagePlan`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-stage-plan.md) | Optional | - | QueryStagePlan getQueryStagePlan() | setQueryStagePlan(QueryStagePlan queryStagePlan) |
| `SubStages` | [`List<QueryStage>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-stage.md) | Optional | - | List<QueryStage> getSubStages() | setSubStages(List<QueryStage> subStages) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.QueryStage;
import java.io.IOException;

QueryStage queryStage = new QueryStage.Builder()
    .stageId(118)
    .state("State0")
    .outputBytes(120)
    .outputRows(146)
    .inputBytes(178)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



