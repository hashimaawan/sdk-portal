# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ


# Class Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `next_token` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `executors_summary` | [`Array[ExecutorsSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/executors-summary.md) | Optional | - |


# Example

```ruby
list_executors_response = ListExecutorsResponse.new(
  'SessionId2',
  'NextToken6',
  [
    ExecutorsSummary.new(
      'ExecutorId8',
      ExecutorType2Enum::GATEWAY,
      128,
      236,
      ExecutorState3Enum::TERMINATED,
      42
    )
  ]
)
```



