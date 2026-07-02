# Query Execution 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uMQ


# Class Name

`QueryExecution1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `query` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `statement_type` | [`StatementType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/statement-type-1.md) | Optional | - |
| `result_configuration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-configuration-1.md) | Optional | - |
| `result_reuse_configuration` | [`ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-reuse-configuration-1.md) | Optional | - |
| `query_execution_context` | [`QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-execution-context-1.md) | Optional | - |
| `status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status.md) | Optional | - |
| `statistics` | [`Statistics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/statistics.md) | Optional | - |
| `work_group` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-version-1.md) | Optional | - |
| `execution_parameters` | `Array[String]` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `substatement_type` | `String` | Optional | - |


# Example

```ruby
query_execution1 = QueryExecution1.new(
  'QueryExecutionId0',
  'Query6',
  StatementType1Enum::UTILITY,
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
  ResultReuseConfiguration1.new(
    ResultReuseByAgeConfiguration2.new(
      false,
      26
    )
  ),
  QueryExecutionContext1.new,
  Status.new(
    envrr,
    nil,
    DateTimeHelper.from_rfc3339(nil),
    DateTimeHelper.from_rfc3339(nil),
    AthenaError2.new
  ),
  Statistics.new(
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    ResultReuseInformation2.new
  ),
  nil,
  EngineVersion1.new,
  []
)
```



