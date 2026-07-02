# Query Runtime Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3M

The query execution timeline, statistics on input and output rows and bytes, and the different query stages that form the query execution plan.

*This model accepts additional fields of type Object.*


# Class Name

`QueryRuntimeStatistics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Timeline` | [`QueryRuntimeStatisticsTimeline`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-runtime-statistics-timeline.md) | Optional | Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time. | QueryRuntimeStatisticsTimeline getTimeline() | setTimeline(QueryRuntimeStatisticsTimeline timeline) |
| `Rows` | [`QueryRuntimeStatisticsRows`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-runtime-statistics-rows.md) | Optional | Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query. | QueryRuntimeStatisticsRows getRows() | setRows(QueryRuntimeStatisticsRows rows) |
| `OutputStage` | [`OutputStage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/output-stage.md) | Optional | - | OutputStage getOutputStage() | setOutputStage(OutputStage outputStage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.OutputStage;
import com.amazonaws.useast1.athena.models.QueryRuntimeStatistics;
import com.amazonaws.useast1.athena.models.QueryRuntimeStatisticsRows;
import com.amazonaws.useast1.athena.models.QueryRuntimeStatisticsTimeline;
import java.io.IOException;

QueryRuntimeStatistics queryRuntimeStatistics = new QueryRuntimeStatistics.Builder()
    .timeline(new QueryRuntimeStatisticsTimeline.Builder()
        .queryQueueTimeInMillis(156)
        .queryPlanningTimeInMillis(82)
        .engineExecutionTimeInMillis(112)
        .serviceProcessingTimeInMillis(126)
        .totalExecutionTimeInMillis(106)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .rows(new QueryRuntimeStatisticsRows.Builder()
        .inputRows(230)
        .inputBytes(250)
        .outputBytes(36)
        .outputRows(230)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .outputStage(new OutputStage.Builder()
        .stageId(130)
        .state("State0")
        .outputBytes(108)
        .outputRows(158)
        .inputBytes(190)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



