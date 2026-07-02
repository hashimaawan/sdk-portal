# Layout

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkxheW91dA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Layout`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `num_nodes` | `int` | Optional | - |
| `sizes` | `List[str]` | Optional, Read-only | An array of objects containing the slugs available with various node counts |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.layout import Layout

layout = Layout(
    num_nodes=1,
    sizes=[
        'db-s-1vcpu-1gb',
        'db-s-1vcpu-2gb'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



