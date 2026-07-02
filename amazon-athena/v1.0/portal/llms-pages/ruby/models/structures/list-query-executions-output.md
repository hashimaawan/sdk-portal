# List Query Executions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListQueryExecutionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_ids` | `Array[String]` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_query_executions_output = ListQueryExecutionsOutput.new(
  query_execution_ids: [
    'QueryExecutionIds3',
    'QueryExecutionIds4'
  ],
  next_token: 'NextToken6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



