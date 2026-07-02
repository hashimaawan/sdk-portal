# V2 Functions Namespaces Triggers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `function` | `str` | Required | Name of function(action) that exists in the given namespace. |
| `is_enabled` | `bool` | Required | Indicates weather the trigger is paused or unpaused. |
| `name` | `str` | Required | The trigger's unique name within the namespace. |
| `scheduled_details` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/scheduled-details.md) | Required | Trigger details for SCHEDULED type, where body is optional. |
| `mtype` | `str` | Required | One of different type of triggers. Currently only SCHEDULED is supported. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.body import Body
from digitaloceanapi.models.scheduled_details import ScheduledDetails
from digitaloceanapi.models.v_2_functions_namespaces_triggers_request import V2FunctionsNamespacesTriggersRequest

v_2_functions_namespaces_triggers_request = V2FunctionsNamespacesTriggersRequest(
    function='hello',
    is_enabled=True,
    name='my trigger',
    scheduled_details=ScheduledDetails(
        cron='* * * * *',
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
    mtype='SCHEDULED',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



