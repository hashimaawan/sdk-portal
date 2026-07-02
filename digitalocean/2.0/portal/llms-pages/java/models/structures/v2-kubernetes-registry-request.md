# V2 Kubernetes Registry Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBSZWdpc3RyeSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesRegistryRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ClusterUuids` | `List<String>` | Optional | An array containing the UUIDs of Kubernetes clusters. | List<String> getClusterUuids() | setClusterUuids(List<String> clusterUuids) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2KubernetesRegistryRequest;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesRegistryRequest v2KubernetesRegistryRequest = new V2KubernetesRegistryRequest.Builder()
    .clusterUuids(Arrays.asList(
        "bd5f5959-5e1e-4205-a714-a914373942af",
        "50c2f44c-011d-493e-aee5-361a4a0d1844"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



