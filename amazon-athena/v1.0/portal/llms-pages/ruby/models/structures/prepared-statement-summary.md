# Prepared Statement Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50U3VtbWFyeQ

The name and last modified time of the prepared statement.

*This model accepts additional fields of type Object.*


# Class Name

`PreparedStatementSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statement_name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `last_modified_time` | `DateTime` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
prepared_statement_summary = PreparedStatementSummary.new(
  statement_name: 'StatementName0',
  last_modified_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



