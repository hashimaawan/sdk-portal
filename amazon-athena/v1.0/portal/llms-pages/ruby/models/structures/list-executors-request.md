# List Executors Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ListExecutorsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `executor_state_filter` | [`ExecutorState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/executor-state-1.md) | Optional | - |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_executors_request = ListExecutorsRequest.new(
  session_id: 'SessionId6',
  executor_state_filter: ExecutorState1::REGISTERED,
  max_results: 100,
  next_token: 'NextToken2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



