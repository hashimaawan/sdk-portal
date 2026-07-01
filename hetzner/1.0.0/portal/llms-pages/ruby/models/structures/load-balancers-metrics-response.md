# Load Balancers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwTWV0cmljcyUyNTIwUmVzcG9uc2U


# Class Name

`LoadBalancersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/metrics.md) | Required | - |


# Example

```ruby
load_balancers_metrics_response = LoadBalancersMetricsResponse.new(
  Metrics.new(
    '2017-01-01T23:00:00+00:00',
    '2017-01-01T00:00:00+00:00',
    60,
    {
      'name_of_timeseries': TimeSeries.new(
        [
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



