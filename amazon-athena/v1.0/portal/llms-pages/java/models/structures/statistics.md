# Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXRpc3RpY3M


# Class Name

`Statistics`


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


# Example

```java
import com.amazonaws.useast1.athena.models.Statistics;

Statistics statistics = new Statistics.Builder()
    .engineExecutionTimeInMillis(72)
    .dataScannedInBytes(60)
    .dataManifestLocation("DataManifestLocation0")
    .totalExecutionTimeInMillis(146)
    .queryQueueTimeInMillis(116)
    .build();
```



