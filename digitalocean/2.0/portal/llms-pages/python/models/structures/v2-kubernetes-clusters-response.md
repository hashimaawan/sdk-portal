# V2 Kubernetes Clusters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetes_clusters` | [`List[KubernetesCluster]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/kubernetes-cluster.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.kubernetes_cluster import KubernetesCluster
from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.node_pool import NodePool
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.v_2_kubernetes_clusters_response import V2KubernetesClustersResponse

v_2_kubernetes_clusters_response = V2KubernetesClustersResponse(
    meta=Meta(
        total=1,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    kubernetes_clusters=[
        KubernetesCluster(
            name='name2',
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
            region='region8',
            version='version8',
            auto_upgrade=False,
            cluster_subnet='cluster_subnet4',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            endpoint='endpoint0',
            ha=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        KubernetesCluster(
            name='name2',
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
            region='region8',
            version='version8',
            auto_upgrade=False,
            cluster_subnet='cluster_subnet4',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            endpoint='endpoint0',
            ha=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        KubernetesCluster(
            name='name2',
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
            region='region8',
            version='version8',
            auto_upgrade=False,
            cluster_subnet='cluster_subnet4',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            endpoint='endpoint0',
            ha=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='last6',
            next='next2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



