# V2 Kubernetes Clusters Node Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersNodePoolsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NodePool` | [`NodePool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/node-pool.md) | Optional | - | NodePool getNodePool() | setNodePool(NodePool nodePool) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Node;
import com.digitalocean.api.models.NodePool;
import com.digitalocean.api.models.State1;
import com.digitalocean.api.models.Status10;
import com.digitalocean.api.models.V2KubernetesClustersNodePoolsResponse1;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2KubernetesClustersNodePoolsResponse1 v2KubernetesClustersNodePoolsResponse1 = new V2KubernetesClustersNodePoolsResponse1.Builder()
    .nodePool(new NodePool.Builder(
        "s-1vcpu-2gb",
        3,
        "new-pool"
    )
    .autoScale(true)
    .id(UUID.fromString("cdda885e-7663-40c8-bc74-3a036c66545d"))
    .labels(null)
    .maxNodes(6)
    .minNodes(3)
    .nodes(Arrays.asList(
            new Node.Builder()
                .createdAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
                .dropletId(" ")
                .id(UUID.fromString("478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f"))
                .name(" ")
                .status(new Status10.Builder()
                    .state(State1.PROVISIONING)
                    .build())
                .updatedAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
                .build(),
            new Node.Builder()
                .createdAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
                .dropletId(" ")
                .id(UUID.fromString("ad12e744-c2a9-473d-8aa9-be5680500eb1"))
                .name(" ")
                .status(new Status10.Builder()
                    .state(State1.PROVISIONING)
                    .build())
                .updatedAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
                .build(),
            new Node.Builder()
                .createdAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
                .dropletId(" ")
                .id(UUID.fromString("e46e8d07-f58f-4ff1-9737-97246364400e"))
                .name(" ")
                .status(new Status10.Builder()
                    .state(State1.PROVISIONING)
                    .build())
                .updatedAt(DateTimeHelper.fromRfc8601DateTime("2018-11-15T16:00:11Z"))
                .build()
        ))
    .tags(Arrays.asList(
            "production",
            "web-team",
            "front-end",
            "k8s",
            "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
            "k8s:worker"
        ))
    .taints(Arrays.asList(

        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



