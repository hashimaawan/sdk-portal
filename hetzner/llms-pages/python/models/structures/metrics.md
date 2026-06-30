# Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRk1ldHJpY3M


# Class Name

`Metrics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `end` | `str` | Required | End of period of metrics reported (in ISO-8601 format) |
| `start` | `str` | Required | Start of period of metrics reported (in ISO-8601 format) |
| `step` | `float` | Required | Resolution of results in seconds. |
| `time_series` | [`Dict[str, TimeSeries]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/time-series.md) | Required | Hash with timeseries information, containing the name of timeseries as key |


# Example

```python
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
            ]
        )
    }
)
```



