# V2 Kubernetes Clusters Node Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `node_pool` | [`NodePool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/node-pool.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.node import Node
from digitaloceanapi.models.node_pool import NodePool
from digitaloceanapi.models.state_1 import State1
from digitaloceanapi.models.status_10 import Status10
from digitaloceanapi.models.v_2_kubernetes_clusters_node_pools_response_1 import V2KubernetesClustersNodePoolsResponse1

v_2_kubernetes_clusters_node_pools_response_1 = V2KubernetesClustersNodePoolsResponse1(
    node_pool=NodePool(
        size='s-1vcpu-2gb',
        count=3,
        name='new-pool',
        auto_scale=True,
        id='cdda885e-7663-40c8-bc74-3a036c66545d',
        labels=None,
        max_nodes=6,
        min_nodes=3,
        nodes=[
            Node(
                created_at=dateutil.parser.parse('2018-11-15T16:00:11Z'),
                droplet_id=' ',
                id='478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f',
                name=' ',
                status=Status10(
                    state=State1.PROVISIONING
                ),
                updated_at=dateutil.parser.parse('2018-11-15T16:00:11Z')
            ),
            Node(
                created_at=dateutil.parser.parse('2018-11-15T16:00:11Z'),
                droplet_id=' ',
                id='ad12e744-c2a9-473d-8aa9-be5680500eb1',
                name=' ',
                status=Status10(
                    state=State1.PROVISIONING
                ),
                updated_at=dateutil.parser.parse('2018-11-15T16:00:11Z')
            ),
            Node(
                created_at=dateutil.parser.parse('2018-11-15T16:00:11Z'),
                droplet_id=' ',
                id='e46e8d07-f58f-4ff1-9737-97246364400e',
                name=' ',
                status=Status10(
                    state=State1.PROVISIONING
                ),
                updated_at=dateutil.parser.parse('2018-11-15T16:00:11Z')
            )
        ],
        tags=[
            'production',
            'web-team',
            'front-end',
            'k8s',
            'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
            'k8s:worker'
        ],
        taints=[],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



