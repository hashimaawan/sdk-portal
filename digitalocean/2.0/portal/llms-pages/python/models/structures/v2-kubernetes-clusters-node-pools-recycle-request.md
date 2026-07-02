# V2 Kubernetes Clusters Node Pools Recycle Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlY3ljbGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsRecycleRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nodes` | `List[str]` | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_kubernetes_clusters_node_pools_recycle_request import V2KubernetesClustersNodePoolsRecycleRequest

v_2_kubernetes_clusters_node_pools_recycle_request = V2KubernetesClustersNodePoolsRecycleRequest(
    nodes=[
        'd8db5e1a-6103-43b5-a7b3-8a948210a9fc'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



