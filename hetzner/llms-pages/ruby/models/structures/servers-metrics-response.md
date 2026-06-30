# Servers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyME1ldHJpY3MlMjUyMFJlc3BvbnNl


# Class Name

`ServersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/metrics.md) | Required | - |


# Example

```ruby
servers_metrics_response = ServersMetricsResponse.new(
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



