# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `next_token` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `executors_summary` | [`Array[ExecutorsSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/executors-summary.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_executors_response = ListExecutorsResponse.new(
  session_id: 'SessionId2',
  next_token: 'NextToken6',
  executors_summary: [
    ExecutorsSummary.new(
      executor_id: 'ExecutorId8',
      executor_type: ExecutorType2::GATEWAY,
      start_date_time: 128,
      termination_date_time: 236,
      executor_state: ExecutorState3::TERMINATED,
      executor_size: 42,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



