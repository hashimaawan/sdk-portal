# Get Query Runtime Statistics Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`GetQueryRuntimeStatisticsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_query_runtime_statistics_input = GetQueryRuntimeStatisticsInput.new(
  query_execution_id: 'QueryExecutionId0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



