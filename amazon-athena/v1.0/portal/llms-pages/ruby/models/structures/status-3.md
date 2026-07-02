# Status 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXR1czM

*This model accepts additional fields of type Object.*


# Class Name

`Status3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `start_date_time` | `DateTime` | Optional | - |
| `last_modified_date_time` | `DateTime` | Optional | - |
| `end_date_time` | `DateTime` | Optional | - |
| `idle_since_date_time` | `DateTime` | Optional | - |
| `state` | [`SessionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/session-state-1.md) | Optional | - |
| `state_change_reason` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
status3 = Status3.new(
  start_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  last_modified_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  end_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  idle_since_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  state: SessionState1::CREATING,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



