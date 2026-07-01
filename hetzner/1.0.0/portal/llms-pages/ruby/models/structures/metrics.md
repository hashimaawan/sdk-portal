# Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRk1ldHJpY3M


# Class Name

`Metrics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mend` | `String` | Required | End of period of metrics reported (in ISO-8601 format) |
| `start` | `String` | Required | Start of period of metrics reported (in ISO-8601 format) |
| `step` | `Float` | Required | Resolution of results in seconds. |
| `time_series` | [`Hash[String, TimeSeries]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/time-series.md) | Required | Hash with timeseries information, containing the name of timeseries as key |


# Example

```ruby
metrics = Metrics.new(
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
```



