# V2 Kubernetes Clusters Upgrades Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXBncmFkZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2KubernetesClustersUpgradesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available_upgrade_versions` | [`List[AvailableUpgradeVersion]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/available-upgrade-version.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.available_upgrade_version import AvailableUpgradeVersion
from digitaloceanapi.models.v_2_kubernetes_clusters_upgrades_response import V2KubernetesClustersUpgradesResponse

v_2_kubernetes_clusters_upgrades_response = V2KubernetesClustersUpgradesResponse(
    available_upgrade_versions=[
        AvailableUpgradeVersion(
            kubernetes_version='kubernetes_version0',
            slug='slug2',
            supported_features=[
                'supported_features3'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        AvailableUpgradeVersion(
            kubernetes_version='kubernetes_version0',
            slug='slug2',
            supported_features=[
                'supported_features3'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        AvailableUpgradeVersion(
            kubernetes_version='kubernetes_version0',
            slug='slug2',
            supported_features=[
                'supported_features3'
            ],
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



