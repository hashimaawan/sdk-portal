# Unprocessed Named Query Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkTmFtZWRRdWVyeUlk

Information about a named query ID that could not be processed.

*This model accepts additional fields of type Object.*


# Class Name

`UnprocessedNamedQueryId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `error_code` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `error_message` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
unprocessed_named_query_id = UnprocessedNamedQueryId.new(
  named_query_id: 'NamedQueryId8',
  error_code: 'ErrorCode6',
  error_message: 'ErrorMessage6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



