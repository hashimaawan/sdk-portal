# Servers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyME1ldHJpY3MlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`ServersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/metrics.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.metrics import Metrics
from hetznercloudapi.models.servers_metrics_response import ServersMetricsResponse
from hetznercloudapi.models.time_series import TimeSeries

servers_metrics_response = ServersMetricsResponse(
    metrics=Metrics(
        end='2017-01-01T23:00:00+00:00',
        start='2017-01-01T00:00:00+00:00',
        step=60,
        time_series={
            'name_of_timeseries': TimeSeries(
                values=[
                    [
                        1435781470.622,
                        '42'
                    ],
                    [
                        1435781471.622,
                        '43'
                    ]
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        },
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



