# V2 Functions Namespaces Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namespace` | [`Namespace`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/namespace.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.namespace import Namespace
from digitaloceanapi.models.v_2_functions_namespaces_response_1 import V2FunctionsNamespacesResponse1

v_2_functions_namespaces_response_1 = V2FunctionsNamespacesResponse1(
    namespace=Namespace(
        api_host='api_host2',
        created_at='created_at0',
        key='key2',
        label='label2',
        namespace='namespace0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



