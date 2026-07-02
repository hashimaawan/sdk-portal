# Batch Get Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`BatchGetPreparedStatementInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statement_names` | `Array[String]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
batch_get_prepared_statement_input = BatchGetPreparedStatementInput.new(
  prepared_statement_names: [
    'PreparedStatementNames0',
    'PreparedStatementNames1'
  ],
  work_group: 'WorkGroup8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



