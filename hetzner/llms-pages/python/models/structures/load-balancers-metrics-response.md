# Load Balancers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwTWV0cmljcyUyNTIwUmVzcG9uc2U


# Class Name

`LoadBalancersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/metrics.md) | Required | - |


# Example

```python
from hetznercloudapi.models.load_balancers_metrics_response import LoadBalancersMetricsResponse
from hetznercloudapi.models.metrics import Metrics
from hetznercloudapi.models.time_series import TimeSeries

load_balancers_metrics_response = LoadBalancersMetricsResponse(
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
                ]
            )
        }
    )
)
```



