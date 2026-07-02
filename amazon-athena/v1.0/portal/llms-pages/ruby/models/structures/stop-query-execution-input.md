# Stop Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0b3BRdWVyeUV4ZWN1dGlvbklucHV0

*This model accepts additional fields of type Object.*


# Class Name

`StopQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
stop_query_execution_input = StopQueryExecutionInput.new(
  query_execution_id: 'QueryExecutionId6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



