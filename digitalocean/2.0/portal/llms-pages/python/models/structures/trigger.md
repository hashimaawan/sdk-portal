# Trigger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlRyaWdnZXI

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Trigger`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `str` | Optional | UTC time string. |
| `function` | `str` | Optional | Name of function(action) that exists in the given namespace. |
| `is_enabled` | `bool` | Optional | Indicates weather the trigger is paused or unpaused. |
| `name` | `str` | Optional | The trigger's unique name within the namespace. |
| `namespace` | `str` | Optional | A unique string format of UUID with a prefix fn-. |
| `scheduled_details` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. |
| `scheduled_runs` | [`ScheduledRuns`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/scheduled-runs.md) | Optional | - |
| `mtype` | `str` | Optional | String which indicates the type of trigger source like SCHEDULED. |
| `updated_at` | `str` | Optional | UTC time string. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.trigger import Trigger

trigger = Trigger(
    created_at='2022-11-11T04:16:45Z',
    function='hello',
    is_enabled=True,
    name='my trigger',
    namespace='fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx',
    mtype='SCHEDULED',
    updated_at='2022-11-11T04:16:45Z',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



