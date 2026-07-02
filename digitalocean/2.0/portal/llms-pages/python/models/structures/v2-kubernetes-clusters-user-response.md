# V2 Kubernetes Clusters User Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXNlciUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersUserResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetes_cluster_user` | [`KubernetesClusterUser`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/kubernetes-cluster-user.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.kubernetes_cluster_user import KubernetesClusterUser
from digitaloceanapi.models.v_2_kubernetes_clusters_user_response import V2KubernetesClustersUserResponse

v_2_kubernetes_clusters_user_response = V2KubernetesClustersUserResponse(
    kubernetes_cluster_user=KubernetesClusterUser(
        groups=[
            'groups8'
        ],
        username='username6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



