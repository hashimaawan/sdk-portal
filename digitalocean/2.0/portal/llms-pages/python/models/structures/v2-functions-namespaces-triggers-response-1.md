# V2 Functions Namespaces Triggers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `trigger` | [`Trigger`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/trigger.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.trigger import Trigger
from digitaloceanapi.models.v_2_functions_namespaces_triggers_response_1 import V2FunctionsNamespacesTriggersResponse1

v_2_functions_namespaces_triggers_response_1 = V2FunctionsNamespacesTriggersResponse1(
    trigger=Trigger(
        created_at='created_at6',
        function='function6',
        is_enabled=False,
        name='name8',
        namespace='namespace4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



