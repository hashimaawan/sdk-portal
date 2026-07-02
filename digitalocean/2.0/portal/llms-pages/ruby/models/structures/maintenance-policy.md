# Maintenance Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk1haW50ZW5hbmNlUG9saWN5

An object specifying the maintenance window policy for the Kubernetes cluster.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`MaintenancePolicy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `day` | [`Day`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/day.md) | Optional | The day of the maintenance window policy. May be one of `monday` through `sunday`, or `any` to indicate an arbitrary week day. |
| `duration` | `String` | Optional, Read-only | The duration of the maintenance window policy in human-readable format. |
| `start_time` | `String` | Optional | The start time in UTC of the maintenance window policy in 24-hour clock format / HH:MM notation (e.g., `15:00`). |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
maintenance_policy = MaintenancePolicy.new(
  day: Day::ANY,
  duration: '4h0m0s',
  start_time: '12:00',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



