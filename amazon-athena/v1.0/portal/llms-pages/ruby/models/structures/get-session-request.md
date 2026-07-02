# Get Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`GetSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_session_request = GetSessionRequest.new(
  session_id: 'SessionId4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



