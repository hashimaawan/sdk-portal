# Batch Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`BatchGetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statements` | [`Array[PreparedStatement]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/prepared-statement.md) | Optional | - |
| `unprocessed_prepared_statement_names` | [`Array[UnprocessedPreparedStatementName]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/unprocessed-prepared-statement-name.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
batch_get_prepared_statement_output = BatchGetPreparedStatementOutput.new(
  prepared_statements: [
    PreparedStatement.new(
      statement_name: 'StatementName2',
      query_statement: 'QueryStatement6',
      work_group_name: 'WorkGroupName6',
      description: 'Description2',
      last_modified_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    PreparedStatement.new(
      statement_name: 'StatementName2',
      query_statement: 'QueryStatement6',
      work_group_name: 'WorkGroupName6',
      description: 'Description2',
      last_modified_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    PreparedStatement.new(
      statement_name: 'StatementName2',
      query_statement: 'QueryStatement6',
      work_group_name: 'WorkGroupName6',
      description: 'Description2',
      last_modified_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  unprocessed_prepared_statement_names: [
    UnprocessedPreparedStatementName.new(
      statement_name: 'StatementName0',
      error_code: 'ErrorCode2',
      error_message: 'ErrorMessage8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



