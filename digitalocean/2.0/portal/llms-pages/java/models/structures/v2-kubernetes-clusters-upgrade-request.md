# V2 Kubernetes Clusters Upgrade Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXBncmFkZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersUpgradeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Version` | `String` | Optional | The slug identifier for the version of Kubernetes that the cluster will be upgraded to. | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2KubernetesClustersUpgradeRequest;
import java.io.IOException;

V2KubernetesClustersUpgradeRequest v2KubernetesClustersUpgradeRequest = new V2KubernetesClustersUpgradeRequest.Builder()
    .version("1.16.13-do.0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



