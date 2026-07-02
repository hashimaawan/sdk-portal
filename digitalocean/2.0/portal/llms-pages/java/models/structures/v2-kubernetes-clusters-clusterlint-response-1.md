# V2 Kubernetes Clusters Clusterlint Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersClusterlintResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RunId` | `String` | Optional | ID of the clusterlint run that can be used later to fetch the diagnostics. | String getRunId() | setRunId(String runId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2KubernetesClustersClusterlintResponse1;
import java.io.IOException;

V2KubernetesClustersClusterlintResponse1 v2KubernetesClustersClusterlintResponse1 = new V2KubernetesClustersClusterlintResponse1.Builder()
    .runId("50c2f44c-011d-493e-aee5-361a4a0d1844")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



