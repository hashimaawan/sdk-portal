# Get Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`GetSessionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `WorkGroup` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `EngineVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getEngineVersion() | setEngineVersion(String engineVersion) |
| `EngineConfiguration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/engine-configuration-1.md) | Optional | - | EngineConfiguration1 getEngineConfiguration() | setEngineConfiguration(EngineConfiguration1 engineConfiguration) |
| `NotebookVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getNotebookVersion() | setNotebookVersion(String notebookVersion) |
| `SessionConfiguration` | [`SessionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/session-configuration-2.md) | Optional | - | SessionConfiguration2 getSessionConfiguration() | setSessionConfiguration(SessionConfiguration2 sessionConfiguration) |
| `Status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/status-3.md) | Optional | - | Status3 getStatus() | setStatus(Status3 status) |
| `Statistics` | [`Statistics3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/statistics-3.md) | Optional | - | Statistics3 getStatistics() | setStatistics(Statistics3 statistics) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.AdditionalConfigs;
import com.amazonaws.useast1.athena.models.EngineConfiguration1;
import com.amazonaws.useast1.athena.models.GetSessionResponse;
import java.io.IOException;

GetSessionResponse getSessionResponse = new GetSessionResponse.Builder()
    .sessionId("SessionId6")
    .description("Description4")
    .workGroup("WorkGroup4")
    .engineVersion("EngineVersion8")
    .engineConfiguration(new EngineConfiguration1.Builder(
        94
    )
    .coordinatorDpuSize(1)
    .defaultExecutorDpuSize(1)
    .additionalConfigs(new AdditionalConfigs.Builder()
        .additionalProperty("exampleAdditionalProperty", "AdditionalConfigs_additionalProperties5")
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



