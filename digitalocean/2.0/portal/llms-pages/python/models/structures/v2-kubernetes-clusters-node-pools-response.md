# V2 Kubernetes Clusters Node Pools Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `node_pools` | [`List[NodePool]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/node-pool.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.node_pool import NodePool
from digitaloceanapi.models.v_2_kubernetes_clusters_node_pools_response import V2KubernetesClustersNodePoolsResponse

v_2_kubernetes_clusters_node_pools_response = V2KubernetesClustersNodePoolsResponse(
    node_pools=[
        NodePool(
            size='size6',
            count=206,
            name='name4',
            auto_scale=False,
            id='000013be-0000-0000-0000-000000000000',
            labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
            max_nodes=118,
            min_nodes=54,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        NodePool(
            size='size6',
            count=206,
            name='name4',
            auto_scale=False,
            id='000013be-0000-0000-0000-000000000000',
            labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
            max_nodes=118,
            min_nodes=54,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



