# Get Query Results Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c0lucHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetQueryResultsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1000` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_query_results_input = GetQueryResultsInput.new(
  query_execution_id: 'QueryExecutionId4',
  next_token: 'NextToken0',
  max_results: 116,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



