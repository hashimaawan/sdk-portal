# Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRk1ldHJpY3M

*This model accepts additional fields of type Object.*


# Class Name

`Metrics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mend` | `String` | Required | End of period of metrics reported (in ISO-8601 format) |
| `start` | `String` | Required | Start of period of metrics reported (in ISO-8601 format) |
| `step` | `Float` | Required | Resolution of results in seconds. |
| `time_series` | [`Hash[String, TimeSeries]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/time-series.md) | Required | Hash with timeseries information, containing the name of timeseries as key |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
metrics = Metrics.new(
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
)
```



