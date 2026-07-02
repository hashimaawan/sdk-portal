# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state_filter` | [`SessionState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/session-state-3.md) | Optional | - |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_sessions_request = ListSessionsRequest.new(
  work_group: 'WorkGroup8',
  state_filter: SessionState3::IDLE,
  max_results: 100,
  next_token: 'NextToken6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



