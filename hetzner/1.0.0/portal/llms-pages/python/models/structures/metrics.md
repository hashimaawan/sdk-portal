# Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRk1ldHJpY3M

*This model accepts additional fields of type Any.*


# Class Name

`Metrics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `end` | `str` | Required | End of period of metrics reported (in ISO-8601 format) |
| `start` | `str` | Required | Start of period of metrics reported (in ISO-8601 format) |
| `step` | `float` | Required | Resolution of results in seconds. |
| `time_series` | [`Dict[str, TimeSeries]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/time-series.md) | Required | Hash with timeseries information, containing the name of timeseries as key |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.metrics import Metrics
from hetznercloudapi.models.time_series import TimeSeries

metrics = Metrics(
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
)
```



