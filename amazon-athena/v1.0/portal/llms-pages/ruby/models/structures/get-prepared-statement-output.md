# Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50T3V0cHV0


# Class Name

`GetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statement` | [`PreparedStatement1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/prepared-statement-1.md) | Optional | - |


# Example

```ruby
get_prepared_statement_output = GetPreparedStatementOutput.new(
  PreparedStatement1.new(
    'StatementName4',
    'QueryStatement8',
    'WorkGroupName8',
    'Description0',
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z')
  )
)
```



