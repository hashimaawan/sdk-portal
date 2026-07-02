# V2 Kubernetes Clusters Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_upgrade` | `bool` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `False` |
| `ha` | `bool` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `False` |
| `maintenance_policy` | [`MaintenancePolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. |
| `name` | `str` | Required | A human-readable name for a Kubernetes cluster. |
| `surge_upgrade` | `bool` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `False` |
| `tags` | `List[str]` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.day import Day
from digitaloceanapi.models.maintenance_policy import MaintenancePolicy
from digitaloceanapi.models.v_2_kubernetes_clusters_request import V2KubernetesClustersRequest

v_2_kubernetes_clusters_request = V2KubernetesClustersRequest(
    name='prod-cluster-01',
    auto_upgrade=True,
    ha=True,
    maintenance_policy=MaintenancePolicy(
        day=Day.ANY,
        duration='duration4',
        start_time='start_time2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    surge_upgrade=True,
    tags=[
        'k8s',
        'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
        'production',
        'web-team'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



