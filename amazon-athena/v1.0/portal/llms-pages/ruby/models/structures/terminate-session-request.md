# Terminate Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`TerminateSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
terminate_session_request = TerminateSessionRequest.new(
  session_id: 'SessionId8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



