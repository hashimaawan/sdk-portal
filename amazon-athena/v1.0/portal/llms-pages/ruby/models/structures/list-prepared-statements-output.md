# List Prepared Statements Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHNPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListPreparedStatementsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prepared_statements` | [`Array[PreparedStatementSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/prepared-statement-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_prepared_statements_output = ListPreparedStatementsOutput.new(
  prepared_statements: [
    PreparedStatementSummary.new(
      statement_name: 'StatementName2',
      last_modified_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  next_token: 'NextToken2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



