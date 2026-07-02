# Kubernetes Cluster User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVyVXNlcg

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`KubernetesClusterUser`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `groups` | `List[str]` | Optional | A list of in-cluster groups that the user belongs to. |
| `username` | `str` | Optional | The username for the cluster admin user. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.kubernetes_cluster_user import KubernetesClusterUser

kubernetes_cluster_user = KubernetesClusterUser(
    groups=[
        'k8saas:authenticated'
    ],
    username='sammy@digitalocean.com',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



