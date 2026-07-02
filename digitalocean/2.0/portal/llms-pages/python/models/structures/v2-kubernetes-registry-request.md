# V2 Kubernetes Registry Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBSZWdpc3RyeSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesRegistryRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cluster_uuids` | `List[str]` | Optional | An array containing the UUIDs of Kubernetes clusters. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_kubernetes_registry_request import V2KubernetesRegistryRequest

v_2_kubernetes_registry_request = V2KubernetesRegistryRequest(
    cluster_uuids=[
        'bd5f5959-5e1e-4205-a714-a914373942af',
        '50c2f44c-011d-493e-aee5-361a4a0d1844'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



