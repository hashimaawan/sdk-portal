# Query Runtime Statistics Timeline

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NUaW1lbGluZQ

Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time.


# Class Name

`QueryRuntimeStatisticsTimeline`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryQueueTimeInMillis` | `Integer` | Optional | - | Integer getQueryQueueTimeInMillis() | setQueryQueueTimeInMillis(Integer queryQueueTimeInMillis) |
| `QueryPlanningTimeInMillis` | `Integer` | Optional | - | Integer getQueryPlanningTimeInMillis() | setQueryPlanningTimeInMillis(Integer queryPlanningTimeInMillis) |
| `EngineExecutionTimeInMillis` | `Integer` | Optional | - | Integer getEngineExecutionTimeInMillis() | setEngineExecutionTimeInMillis(Integer engineExecutionTimeInMillis) |
| `ServiceProcessingTimeInMillis` | `Integer` | Optional | - | Integer getServiceProcessingTimeInMillis() | setServiceProcessingTimeInMillis(Integer serviceProcessingTimeInMillis) |
| `TotalExecutionTimeInMillis` | `Integer` | Optional | - | Integer getTotalExecutionTimeInMillis() | setTotalExecutionTimeInMillis(Integer totalExecutionTimeInMillis) |


# Example

```java
import com.amazonaws.useast1.athena.models.QueryRuntimeStatisticsTimeline;

QueryRuntimeStatisticsTimeline queryRuntimeStatisticsTimeline = new QueryRuntimeStatisticsTimeline.Builder()
    .queryQueueTimeInMillis(122)
    .queryPlanningTimeInMillis(48)
    .engineExecutionTimeInMillis(78)
    .serviceProcessingTimeInMillis(96)
    .totalExecutionTimeInMillis(140)
    .build();
```



