# V2 Functions Namespaces Triggers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `triggers` | [`List[Trigger]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/trigger.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.trigger import Trigger
from digitaloceanapi.models.v_2_functions_namespaces_triggers_response import V2FunctionsNamespacesTriggersResponse

v_2_functions_namespaces_triggers_response = V2FunctionsNamespacesTriggersResponse(
    triggers=[
        Trigger(
            created_at='created_at8',
            function='function6',
            is_enabled=False,
            name='name0',
            namespace='namespace2',
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



