# V2 1 Clicks Kubernetes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMEt1YmVybmV0ZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V21ClicksKubernetesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addon_slugs` | `List[str]` | Required | An array of 1-Click Application slugs to be installed to the Kubernetes cluster. |
| `cluster_uuid` | `str` | Required | A unique ID for the Kubernetes cluster to which the 1-Click Applications will be installed. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_21_clicks_kubernetes_request import V21ClicksKubernetesRequest

v_2_1_clicks_kubernetes_request = V21ClicksKubernetesRequest(
    addon_slugs=[
        'kube-state-metrics',
        'loki'
    ],
    cluster_uuid='50a994b6-c303-438f-9495-7e896cfe6b08',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



