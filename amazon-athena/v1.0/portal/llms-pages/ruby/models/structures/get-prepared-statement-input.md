# Get Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50SW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetPreparedStatementInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statement_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_prepared_statement_input = GetPreparedStatementInput.new(
  statement_name: 'StatementName0',
  work_group: 'WorkGroup4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



