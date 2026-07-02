# Diagnostic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkRpYWdub3N0aWM

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Diagnostic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `check_name` | `str` | Optional | The clusterlint check that resulted in the diagnostic. |
| `message` | `str` | Optional | Feedback about the object for users to fix. |
| `object` | [`Object`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | Metadata about the Kubernetes API object the diagnostic is reported on. |
| `severity` | `str` | Optional | Can be one of error, warning or suggestion. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.diagnostic import Diagnostic
from digitaloceanapi.models.object import Object

diagnostic = Diagnostic(
    check_name='unused-config-map',
    message='Unused config map',
    object=Object(
        kind='kind0',
        name='name2',
        namespace='namespace0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    severity='warning',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



