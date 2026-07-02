# V2 Kubernetes Clusters Clusterlint Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersClusterlintResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CompletedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was completed. | LocalDateTime getCompletedAt() | setCompletedAt(LocalDateTime completedAt) |
| `Diagnostics` | [`List<Diagnostic>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/diagnostic.md) | Optional | An array of diagnostics reporting potential problems for the given cluster. | List<Diagnostic> getDiagnostics() | setDiagnostics(List<Diagnostic> diagnostics) |
| `RequestedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was made. | LocalDateTime getRequestedAt() | setRequestedAt(LocalDateTime requestedAt) |
| `RunId` | `String` | Optional | Id of the clusterlint run that can be used later to fetch the diagnostics. | String getRunId() | setRunId(String runId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Diagnostic;
import com.digitalocean.api.models.ObjectType;
import com.digitalocean.api.models.V2KubernetesClustersClusterlintResponse;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesClustersClusterlintResponse v2KubernetesClustersClusterlintResponse = new V2KubernetesClustersClusterlintResponse.Builder()
    .completedAt(DateTimeHelper.fromRfc8601DateTime("2019-10-30T05:34:11Z"))
    .diagnostics(Arrays.asList(
        new Diagnostic.Builder()
            .checkName("check_name8")
            .message("message2")
            .object(new ObjectType.Builder()
                .kind("kind0")
                .name("name2")
                .namespace("namespace0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .severity("severity2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Diagnostic.Builder()
            .checkName("check_name8")
            .message("message2")
            .object(new ObjectType.Builder()
                .kind("kind0")
                .name("name2")
                .namespace("namespace0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .severity("severity2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .requestedAt(DateTimeHelper.fromRfc8601DateTime("2019-10-30T05:34:07Z"))
    .runId("50c2f44c-011d-493e-aee5-361a4a0d1844")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



