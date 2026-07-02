# V2 Kubernetes Clusters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `KubernetesCluster` | [`KubernetesCluster`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/kubernetes-cluster.md) | Optional | - | KubernetesCluster getKubernetesCluster() | setKubernetesCluster(KubernetesCluster kubernetesCluster) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.KubernetesCluster;
import com.digitalocean.api.models.NodePool;
import com.digitalocean.api.models.V2KubernetesClustersResponse1;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2KubernetesClustersResponse1 v2KubernetesClustersResponse1 = new V2KubernetesClustersResponse1.Builder()
    .kubernetesCluster(new KubernetesCluster.Builder(
        "name8",
        Arrays.asList(
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
            .build(),
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
        ),
        "region4",
        "version4"
    )
    .autoUpgrade(false)
    .clusterSubnet("cluster_subnet0")
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .endpoint("endpoint6")
    .ha(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



