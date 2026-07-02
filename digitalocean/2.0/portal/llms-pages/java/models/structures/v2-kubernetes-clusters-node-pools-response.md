# V2 Kubernetes Clusters Node Pools Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersNodePoolsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NodePools` | [`List<NodePool>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/node-pool.md) | Optional | - | List<NodePool> getNodePools() | setNodePools(List<NodePool> nodePools) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.NodePool;
import com.digitalocean.api.models.V2KubernetesClustersNodePoolsResponse;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2KubernetesClustersNodePoolsResponse v2KubernetesClustersNodePoolsResponse = new V2KubernetesClustersNodePoolsResponse.Builder()
    .nodePools(Arrays.asList(
        new NodePool.Builder(
            "size6",
            206,
            "name4"
        )
        .autoScale(false)
        .id(UUID.fromString("000013be-0000-0000-0000-000000000000"))
        .labels(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .maxNodes(118)
        .minNodes(54)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



