# Get Session Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFNlc3Npb25TdGF0dXNSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`GetSessionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status-3.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_session_status_response = GetSessionStatusResponse.new(
  session_id: 'SessionId4',
  status: Status3.new(
    start_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    last_modified_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    end_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    idle_since_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    state: SessionState1::TERMINATING,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



