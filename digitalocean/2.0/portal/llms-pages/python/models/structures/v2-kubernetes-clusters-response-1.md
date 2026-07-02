# V2 Kubernetes Clusters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetes_cluster` | [`KubernetesCluster`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/kubernetes-cluster.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.kubernetes_cluster import KubernetesCluster
from digitaloceanapi.models.node_pool import NodePool
from digitaloceanapi.models.v_2_kubernetes_clusters_response_1 import V2KubernetesClustersResponse1

v_2_kubernetes_clusters_response_1 = V2KubernetesClustersResponse1(
    kubernetes_cluster=KubernetesCluster(
        name='name8',
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
        region='region4',
        version='version4',
        auto_upgrade=False,
        cluster_subnet='cluster_subnet0',
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        endpoint='endpoint6',
        ha=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



