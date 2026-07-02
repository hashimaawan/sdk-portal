# Start Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25JbnB1dA


# Class Name

`StartQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_string` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `client_request_token` | `String` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `query_execution_context` | [`QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-execution-context-1.md) | Optional | - |
| `result_configuration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-configuration-1.md) | Optional | - |
| `work_group` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `execution_parameters` | `Array[String]` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `result_reuse_configuration` | [`ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-reuse-configuration-1.md) | Optional | - |


# Example

```ruby
start_query_execution_input = StartQueryExecutionInput.new(
  'QueryString6',
  'ClientRequestToken8',
  QueryExecutionContext1.new(
    'Database4',
    'Catalog0'
  ),
  ResultConfiguration1.new(
    'OutputLocation0',
    EncryptionConfiguration2.new(
      EncryptionOption1Enum::SSE_S3,
      'KmsKey6'
    ),
    'ExpectedBucketOwner0',
    AclConfiguration1.new(
      S3AclOption1Enum::BUCKET_OWNER_FULL_CONTROL
    )
  ),
  'WorkGroup6',
  [
    'ExecutionParameters8',
    'ExecutionParameters7'
  ],
  ResultReuseConfiguration1.new(
    ResultReuseByAgeConfiguration2.new
  )
)
```



