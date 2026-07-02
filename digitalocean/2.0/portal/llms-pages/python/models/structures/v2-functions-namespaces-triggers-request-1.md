# V2 Functions Namespaces Triggers Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `is_enabled` | `bool` | Optional | Indicates weather the trigger is paused or unpaused. |
| `scheduled_details` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.body import Body
from digitaloceanapi.models.scheduled_details import ScheduledDetails
from digitaloceanapi.models.v_2_functions_namespaces_triggers_request_1 import V2FunctionsNamespacesTriggersRequest1

v_2_functions_namespaces_triggers_request_1 = V2FunctionsNamespacesTriggersRequest1(
    is_enabled=True,
    scheduled_details=ScheduledDetails(
        cron='cron2',
        body=Body(
            name='name6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



