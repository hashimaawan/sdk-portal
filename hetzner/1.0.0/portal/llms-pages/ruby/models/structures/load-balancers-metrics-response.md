# Load Balancers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwTWV0cmljcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/metrics.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancers_metrics_response = LoadBalancersMetricsResponse.new(
  metrics: Metrics.new(
    mend: '2017-01-01T23:00:00+00:00',
    start: '2017-01-01T00:00:00+00:00',
    step: 60,
    time_series: {
      'name_of_timeseries' => TimeSeries.new(
        values: [
          [
            1435781470.622,
            '42'
          ],
          [
            1435781471.622,
            '43'
          ]
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    },
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



