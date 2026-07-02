# V2 Apps Metrics Bandwidth Daily Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsMetricsBandwidthDailyResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_bandwidth_usage` | [`Array[AppBandwidthUsage]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/app-bandwidth-usage.md) | Optional | A list of bandwidth usage details by app. |
| `date` | `DateTime` | Optional | The date for the metrics data. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_metrics_bandwidth_daily_response = V2AppsMetricsBandwidthDailyResponse.new(
  app_bandwidth_usage: [
    AppBandwidthUsage.new(
      app_id: 'app_id4',
      bandwidth_bytes: 'bandwidth_bytes6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    AppBandwidthUsage.new(
      app_id: 'app_id4',
      bandwidth_bytes: 'bandwidth_bytes6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  date: DateTimeHelper.from_rfc3339('2023-01-17T00:00:00Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



