# V2 Kubernetes Clusters Node Pools Recycle Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlY3ljbGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersNodePoolsRecycleRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Nodes` | `List<String>` | Optional | - | List<String> getNodes() | setNodes(List<String> nodes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2KubernetesClustersNodePoolsRecycleRequest;
import java.io.IOException;
import java.util.Arrays;

V2KubernetesClustersNodePoolsRecycleRequest v2KubernetesClustersNodePoolsRecycleRequest = new V2KubernetesClustersNodePoolsRecycleRequest.Builder()
    .nodes(Arrays.asList(
        "d8db5e1a-6103-43b5-a7b3-8a948210a9fc"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



