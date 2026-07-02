# V2 Apps Metrics Bandwidth Daily Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsMetricsBandwidthDailyRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_ids` | `Array[String]` | Required | A list of app IDs to query bandwidth metrics for.<br><br>**Constraints**: *Maximum Items*: `100` |
| `date` | `DateTime` | Optional | Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_metrics_bandwidth_daily_request = V2AppsMetricsBandwidthDailyRequest.new(
  app_ids: [
    '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
    'c2a93513-8d9b-4223-9d61-5e7272c81cf5'
  ],
  date: DateTimeHelper.from_rfc3339('2023-01-17T00:00:00Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



