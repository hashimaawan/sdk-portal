# Batch Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRPdXRwdXQ


# Class Name

`BatchGetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statements` | [`Array[PreparedStatement]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/prepared-statement.md) | Optional | - |
| `unprocessed_prepared_statement_names` | [`Array[UnprocessedPreparedStatementName]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/unprocessed-prepared-statement-name.md) | Optional | - |


# Example

```ruby
batch_get_prepared_statement_output = BatchGetPreparedStatementOutput.new(
  [
    PreparedStatement.new(
      'StatementName2',
      'QueryStatement6',
      'WorkGroupName6',
      'Description2',
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z')
    ),
    PreparedStatement.new(
      'StatementName2',
      'QueryStatement6',
      'WorkGroupName6',
      'Description2',
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z')
    ),
    PreparedStatement.new(
      'StatementName2',
      'QueryStatement6',
      'WorkGroupName6',
      'Description2',
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z')
    )
  ],
  [
    UnprocessedPreparedStatementName.new(
      'StatementName0',
      'ErrorCode2',
      'ErrorMessage8'
    )
  ]
)
```



