# Node Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk5vZGVQb29s

*This model accepts additional fields of type Object.*


# Class Name

`NodePool`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Size` | `String` | Required | The slug identifier for the type of Droplet used as workers in the node pool. | String getSize() | setSize(String size) |
| `AutoScale` | `Boolean` | Optional | A boolean value indicating whether auto-scaling is enabled for this node pool. | Boolean getAutoScale() | setAutoScale(Boolean autoScale) |
| `Count` | `int` | Required | The number of Droplet instances in the node pool. | int getCount() | setCount(int count) |
| `Id` | `UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a specific node pool. | UUID getId() | setId(UUID id) |
| `Labels` | `Object` | Optional | An object containing a set of Kubernetes labels. The keys and are values are both user-defined. | Object getLabels() | setLabels(Object labels) |
| `MaxNodes` | `Integer` | Optional | The maximum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. | Integer getMaxNodes() | setMaxNodes(Integer maxNodes) |
| `MinNodes` | `Integer` | Optional | The minimum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. | Integer getMinNodes() | setMinNodes(Integer minNodes) |
| `Name` | `String` | Required | A human-readable name for the node pool. | String getName() | setName(String name) |
| `Nodes` | [`List<Node>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/node.md) | Optional, Read-only | An object specifying the details of a specific worker node in a node pool. | List<Node> getNodes() | setNodes(List<Node> nodes) |
| `Tags` | `List<String>` | Optional | An array containing the tags applied to the node pool. All node pools are automatically tagged `k8s`, `k8s-worker`, and `k8s:$K8S_CLUSTER_ID`. | List<String> getTags() | setTags(List<String> tags) |
| `Taints` | [`List<Taint>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/taint.md) | Optional | An array of taints to apply to all nodes in a pool. Taints will automatically be applied to all existing nodes and any subsequent nodes added to the pool. When a taint is removed, it is removed from all nodes in the pool. | List<Taint> getTaints() | setTaints(List<Taint> taints) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.NodePool;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

NodePool nodePool = new NodePool.Builder(
    "s-1vcpu-2gb",
    3,
    "frontend-pool"
)
.autoScale(true)
.id(UUID.fromString("cdda885e-7663-40c8-bc74-3a036c66545d"))
.labels(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.maxNodes(6)
.minNodes(3)
.tags(Arrays.asList(
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "k8s-worker",
        "production",
        "web-team"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



