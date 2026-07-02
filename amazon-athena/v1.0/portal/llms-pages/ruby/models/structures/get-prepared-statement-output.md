# Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50T3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statement` | [`PreparedStatement1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/prepared-statement-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_prepared_statement_output = GetPreparedStatementOutput.new(
  prepared_statement: PreparedStatement1.new(
    statement_name: 'StatementName4',
    query_statement: 'QueryStatement8',
    work_group_name: 'WorkGroupName8',
    description: 'Description0',
    last_modified_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



