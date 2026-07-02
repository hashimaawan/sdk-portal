# Terminate Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`TerminateSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`SessionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/session-state-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
terminate_session_response = TerminateSessionResponse.new(
  state: SessionState1::CREATING,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



