# Get Query Runtime Statistics Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetQueryRuntimeStatisticsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryRuntimeStatistics` | [`QueryRuntimeStatistics2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-runtime-statistics-2.md) | Optional | - | QueryRuntimeStatistics2 getQueryRuntimeStatistics() | setQueryRuntimeStatistics(QueryRuntimeStatistics2 queryRuntimeStatistics) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.GetQueryRuntimeStatisticsOutput;
import com.amazonaws.useast1.athena.models.OutputStage;
import com.amazonaws.useast1.athena.models.QueryRuntimeStatistics2;
import com.amazonaws.useast1.athena.models.QueryRuntimeStatisticsRows;
import com.amazonaws.useast1.athena.models.QueryRuntimeStatisticsTimeline;
import java.io.IOException;

GetQueryRuntimeStatisticsOutput getQueryRuntimeStatisticsOutput = new GetQueryRuntimeStatisticsOutput.Builder()
    .queryRuntimeStatistics(new QueryRuntimeStatistics2.Builder()
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
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



