# Start Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`StartSessionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `EngineConfiguration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/engine-configuration-1.md) | Required | - | EngineConfiguration1 getEngineConfiguration() | setEngineConfiguration(EngineConfiguration1 engineConfiguration) |
| `NotebookVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getNotebookVersion() | setNotebookVersion(String notebookVersion) |
| `SessionIdleTimeoutInMinutes` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 480` | Integer getSessionIdleTimeoutInMinutes() | setSessionIdleTimeoutInMinutes(Integer sessionIdleTimeoutInMinutes) |
| `ClientRequestToken` | `String` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` | String getClientRequestToken() | setClientRequestToken(String clientRequestToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.AdditionalConfigs;
import com.amazonaws.useast1.athena.models.EngineConfiguration1;
import com.amazonaws.useast1.athena.models.StartSessionRequest;
import java.io.IOException;

StartSessionRequest startSessionRequest = new StartSessionRequest.Builder(
    "WorkGroup2",
    new EngineConfiguration1.Builder(
        94
    )
    .coordinatorDpuSize(1)
    .defaultExecutorDpuSize(1)
    .additionalConfigs(new AdditionalConfigs.Builder()
        .additionalProperty("exampleAdditionalProperty", "AdditionalConfigs_additionalProperties5")
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.description("Description4")
.notebookVersion("NotebookVersion4")
.sessionIdleTimeoutInMinutes(172)
.clientRequestToken("ClientRequestToken4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



