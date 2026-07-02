# V2 Apps Metrics Bandwidth Daily Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsMetricsBandwidthDailyResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_bandwidth_usage` | [`List[AppBandwidthUsage]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/app-bandwidth-usage.md) | Optional | A list of bandwidth usage details by app. |
| `date` | `datetime` | Optional | The date for the metrics data. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.app_bandwidth_usage import AppBandwidthUsage
from digitaloceanapi.models.v_2_apps_metrics_bandwidth_daily_response import V2AppsMetricsBandwidthDailyResponse

v_2_apps_metrics_bandwidth_daily_response = V2AppsMetricsBandwidthDailyResponse(
    app_bandwidth_usage=[
        AppBandwidthUsage(
            app_id='app_id4',
            bandwidth_bytes='bandwidth_bytes6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        AppBandwidthUsage(
            app_id='app_id4',
            bandwidth_bytes='bandwidth_bytes6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    date=dateutil.parser.parse('2023-01-17T00:00:00Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



