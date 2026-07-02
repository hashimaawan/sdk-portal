# V2 Apps Metrics Bandwidth Daily Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsMetricsBandwidthDailyRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_ids` | `List[str]` | Required | A list of app IDs to query bandwidth metrics for.<br><br>**Constraints**: *Maximum Items*: `100` |
| `date` | `datetime` | Optional | Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.v_2_apps_metrics_bandwidth_daily_request import V2AppsMetricsBandwidthDailyRequest

v_2_apps_metrics_bandwidth_daily_request = V2AppsMetricsBandwidthDailyRequest(
    app_ids=[
        '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
        'c2a93513-8d9b-4223-9d61-5e7272c81cf5'
    ],
    date=dateutil.parser.parse('2023-01-17T00:00:00Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



