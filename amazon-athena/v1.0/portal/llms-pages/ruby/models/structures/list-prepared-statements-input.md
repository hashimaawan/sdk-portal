# List Prepared Statements Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHNJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListPreparedStatementsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_prepared_statements_input = ListPreparedStatementsInput.new(
  work_group: 'WorkGroup2',
  next_token: 'NextToken0',
  max_results: 50,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



