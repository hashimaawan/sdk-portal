# Scheduled Runs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlNjaGVkdWxlZFJ1bnM

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`ScheduledRuns`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `last_run_at` | `String` | Optional | Indicates last run time. null value indicates trigger not run yet. |
| `next_run_at` | `String` | Optional | Indicates next run time. null value indicates trigger will not run. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
scheduled_runs = ScheduledRuns.new(
  last_run_at: '2022-11-11T04:16:45Z',
  next_run_at: '2022-11-11T04:16:45Z',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



