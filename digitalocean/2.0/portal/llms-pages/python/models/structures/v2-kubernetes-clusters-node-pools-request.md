# V2 Kubernetes Clusters Node Pools Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_scale` | `bool` | Optional | A boolean value indicating whether auto-scaling is enabled for this node pool. |
| `count` | `int` | Optional | The number of Droplet instances in the node pool. |
| `id` | `uuid\|str` | Optional, Read-only | A unique ID that can be used to identify and reference a specific node pool. |
| `labels` | [`Any`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | An object containing a set of Kubernetes labels. The keys and are values are both user-defined. |
| `max_nodes` | `int` | Optional | The maximum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. |
| `min_nodes` | `int` | Optional | The minimum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. |
| `name` | `str` | Optional | A human-readable name for the node pool. |
| `nodes` | [`List[Node]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/node.md) | Optional, Read-only | An object specifying the details of a specific worker node in a node pool. |
| `tags` | `List[str]` | Optional | An array containing the tags applied to the node pool. All node pools are automatically tagged `k8s`, `k8s-worker`, and `k8s:$K8S_CLUSTER_ID`. |
| `taints` | [`List[Taint]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/taint.md) | Optional | An array of taints to apply to all nodes in a pool. Taints will automatically be applied to all existing nodes and any subsequent nodes added to the pool. When a taint is removed, it is removed from all nodes in the pool. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_kubernetes_clusters_node_pools_request import V2KubernetesClustersNodePoolsRequest

v_2_kubernetes_clusters_node_pools_request = V2KubernetesClustersNodePoolsRequest(
    auto_scale=True,
    count=3,
    id='cdda885e-7663-40c8-bc74-3a036c66545d',
    labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    max_nodes=6,
    min_nodes=3,
    name='frontend-pool',
    tags=[
        'k8s',
        'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
        'k8s-worker',
        'production',
        'web-team'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



