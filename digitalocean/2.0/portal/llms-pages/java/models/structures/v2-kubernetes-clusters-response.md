# V2 Kubernetes Clusters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2KubernetesClustersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `KubernetesClusters` | [`List<KubernetesCluster>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/kubernetes-cluster.md) | Optional | - | List<KubernetesCluster> getKubernetesClusters() | setKubernetesClusters(List<KubernetesCluster> kubernetesClusters) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.KubernetesCluster;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.NodePool;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.V2KubernetesClustersResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2KubernetesClustersResponse v2KubernetesClustersResponse = new V2KubernetesClustersResponse.Builder(
    new Meta.Builder(
        1
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.kubernetesClusters(Arrays.asList(
        new KubernetesCluster.Builder(
            "name2",
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
            "region8",
            "version8"
        )
        .autoUpgrade(false)
        .clusterSubnet("cluster_subnet4")
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .endpoint("endpoint0")
        .ha(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new KubernetesCluster.Builder(
            "name2",
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
            "region8",
            "version8"
        )
        .autoUpgrade(false)
        .clusterSubnet("cluster_subnet4")
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .endpoint("endpoint0")
        .ha(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new KubernetesCluster.Builder(
            "name2",
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
            "region8",
            "version8"
        )
        .autoUpgrade(false)
        .clusterSubnet("cluster_subnet4")
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .endpoint("endpoint0")
        .ha(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("last6")
                .next("next2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



