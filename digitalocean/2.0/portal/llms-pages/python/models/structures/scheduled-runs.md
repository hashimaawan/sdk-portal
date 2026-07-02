# Scheduled Runs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlNjaGVkdWxlZFJ1bnM

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`ScheduledRuns`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `last_run_at` | `str` | Optional | Indicates last run time. null value indicates trigger not run yet. |
| `next_run_at` | `str` | Optional | Indicates next run time. null value indicates trigger will not run. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.scheduled_runs import ScheduledRuns

scheduled_runs = ScheduledRuns(
    last_run_at='2022-11-11T04:16:45Z',
    next_run_at='2022-11-11T04:16:45Z',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



