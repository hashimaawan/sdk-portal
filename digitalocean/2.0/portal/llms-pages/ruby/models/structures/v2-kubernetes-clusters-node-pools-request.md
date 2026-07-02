# V2 Kubernetes Clusters Node Pools Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_scale` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether auto-scaling is enabled for this node pool. |
| `count` | `Integer` | Optional | The number of Droplet instances in the node pool. |
| `id` | `UUID \| String` | Optional, Read-only | A unique ID that can be used to identify and reference a specific node pool. |
| `labels` | [`Object`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | An object containing a set of Kubernetes labels. The keys and are values are both user-defined. |
| `max_nodes` | `Integer` | Optional | The maximum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. |
| `min_nodes` | `Integer` | Optional | The minimum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. |
| `name` | `String` | Optional | A human-readable name for the node pool. |
| `nodes` | [`Array[Node]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/node.md) | Optional, Read-only | An object specifying the details of a specific worker node in a node pool. |
| `tags` | `Array[String]` | Optional | An array containing the tags applied to the node pool. All node pools are automatically tagged `k8s`, `k8s-worker`, and `k8s:$K8S_CLUSTER_ID`. |
| `taints` | [`Array[Taint]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/taint.md) | Optional | An array of taints to apply to all nodes in a pool. Taints will automatically be applied to all existing nodes and any subsequent nodes added to the pool. When a taint is removed, it is removed from all nodes in the pool. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_kubernetes_clusters_node_pools_request = V2KubernetesClustersNodePoolsRequest.new(
  auto_scale: true,
  count: 3,
  id: 'cdda885e-7663-40c8-bc74-3a036c66545d',
  labels: { 'key1' => 'val1', 'key2' => 'val2' },
  max_nodes: 6,
  min_nodes: 3,
  name: 'frontend-pool',
  tags: [
    'k8s',
    'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
    'k8s-worker',
    'production',
    'web-team'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



