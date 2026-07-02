# Available Upgrade Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkF2YWlsYWJsZVVwZ3JhZGVWZXJzaW9u

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`AvailableUpgradeVersion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetes_version` | `str` | Optional | The upstream version string for the version of Kubernetes provided by a given slug. |
| `slug` | `str` | Optional | The slug identifier for an available version of Kubernetes for use when creating or updating a cluster. The string contains both the upstream version of Kubernetes as well as the DigitalOcean revision. |
| `supported_features` | `List[str]` | Optional | The features available with the version of Kubernetes provided by a given slug. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.available_upgrade_version import AvailableUpgradeVersion

available_upgrade_version = AvailableUpgradeVersion(
    kubernetes_version='1.16.13',
    slug='1.16.13-do.0',
    supported_features=[
        'cluster-autoscaler',
        'docr-integration',
        'token-authentication'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



