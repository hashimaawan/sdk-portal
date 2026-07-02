# Query Execution Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGlzdGljcw

The amount of data scanned during the query execution and the amount of time that it took to execute, and the type of statement that was run.

*This model accepts additional fields of type Object.*


# Class Name

`QueryExecutionStatistics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EngineExecutionTimeInMillis` | `Integer` | Optional | - | Integer getEngineExecutionTimeInMillis() | setEngineExecutionTimeInMillis(Integer engineExecutionTimeInMillis) |
| `DataScannedInBytes` | `Integer` | Optional | - | Integer getDataScannedInBytes() | setDataScannedInBytes(Integer dataScannedInBytes) |
| `DataManifestLocation` | `String` | Optional | - | String getDataManifestLocation() | setDataManifestLocation(String dataManifestLocation) |
| `TotalExecutionTimeInMillis` | `Integer` | Optional | - | Integer getTotalExecutionTimeInMillis() | setTotalExecutionTimeInMillis(Integer totalExecutionTimeInMillis) |
| `QueryQueueTimeInMillis` | `Integer` | Optional | - | Integer getQueryQueueTimeInMillis() | setQueryQueueTimeInMillis(Integer queryQueueTimeInMillis) |
| `QueryPlanningTimeInMillis` | `Integer` | Optional | - | Integer getQueryPlanningTimeInMillis() | setQueryPlanningTimeInMillis(Integer queryPlanningTimeInMillis) |
| `ServiceProcessingTimeInMillis` | `Integer` | Optional | - | Integer getServiceProcessingTimeInMillis() | setServiceProcessingTimeInMillis(Integer serviceProcessingTimeInMillis) |
| `ResultReuseInformation` | [`ResultReuseInformation2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-reuse-information-2.md) | Optional | - | ResultReuseInformation2 getResultReuseInformation() | setResultReuseInformation(ResultReuseInformation2 resultReuseInformation) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.QueryExecutionStatistics;
import java.io.IOException;

QueryExecutionStatistics queryExecutionStatistics = new QueryExecutionStatistics.Builder()
    .engineExecutionTimeInMillis(98)
    .dataScannedInBytes(86)
    .dataManifestLocation("DataManifestLocation2")
    .totalExecutionTimeInMillis(136)
    .queryQueueTimeInMillis(142)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



