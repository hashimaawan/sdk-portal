# Unprocessed Prepared Statement Name

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUHJlcGFyZWRTdGF0ZW1lbnROYW1l

The name of a prepared statement that could not be returned.

*This model accepts additional fields of type Object.*


# Class Name

`UnprocessedPreparedStatementName`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statement_name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `error_code` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `error_message` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
unprocessed_prepared_statement_name = UnprocessedPreparedStatementName.new(
  statement_name: 'StatementName8',
  error_code: 'ErrorCode0',
  error_message: 'ErrorMessage0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



