# V2 Kubernetes Clusters Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing the IDs of resources to be destroyed along with their associated with a Kubernetes cluster.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancers` | `List[str]` | Optional | A list of IDs for associated load balancers to destroy along with the cluster. |
| `volume_snapshots` | `List[str]` | Optional | A list of IDs for associated volume snapshots to destroy along with the cluster. |
| `volumes` | `List[str]` | Optional | A list of IDs for associated volumes to destroy along with the cluster. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_kubernetes_clusters_destroy_with_associated_resources_selective_request import V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest

v_2_kubernetes_clusters_destroy_with_associated_resources_selective_request = V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest(
    load_balancers=[
        '4de7ac8b-495b-4884-9a69-1050c6793cd6'
    ],
    volume_snapshots=[
        'edb0478d-7436-11ea-86e6-0a58ac144b91'
    ],
    volumes=[
        'ba49449a-7435-11ea-b89e-0a58ac14480f'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



