# Trigger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlRyaWdnZXI

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Trigger`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `String` | Optional | UTC time string. |
| `function` | `String` | Optional | Name of function(action) that exists in the given namespace. |
| `is_enabled` | `TrueClass \| FalseClass` | Optional | Indicates weather the trigger is paused or unpaused. |
| `name` | `String` | Optional | The trigger's unique name within the namespace. |
| `namespace` | `String` | Optional | A unique string format of UUID with a prefix fn-. |
| `scheduled_details` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. |
| `scheduled_runs` | [`ScheduledRuns`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/scheduled-runs.md) | Optional | - |
| `type` | `String` | Optional | String which indicates the type of trigger source like SCHEDULED. |
| `updated_at` | `String` | Optional | UTC time string. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
trigger = Trigger.new(
  created_at: '2022-11-11T04:16:45Z',
  function: 'hello',
  is_enabled: true,
  name: 'my trigger',
  namespace: 'fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx',
  type: 'SCHEDULED',
  updated_at: '2022-11-11T04:16:45Z',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



