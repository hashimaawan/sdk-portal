# Create Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVByZXBhcmVkU3RhdGVtZW50SW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`CreatePreparedStatementInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statement_name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `query_statement` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_prepared_statement_input = CreatePreparedStatementInput.new(
  statement_name: 'StatementName6',
  work_group: 'WorkGroup0',
  query_statement: 'QueryStatement0',
  description: 'Description2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



