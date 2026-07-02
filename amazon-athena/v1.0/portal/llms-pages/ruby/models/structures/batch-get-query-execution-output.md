# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_executions` | [`Array[QueryExecution]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-execution.md) | Optional | - |
| `unprocessed_query_execution_ids` | [`Array[UnprocessedQueryExecutionId]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/unprocessed-query-execution-id.md) | Optional | - |


# Example

```ruby
batch_get_query_execution_output = BatchGetQueryExecutionOutput.new(
  [
    QueryExecution.new(
      'QueryExecutionId6',
      'Query0',
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
    ),
    QueryExecution.new(
      'QueryExecutionId6',
      'Query0',
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
  ],
  [
    UnprocessedQueryExecutionId.new(
      'QueryExecutionId6',
      'ErrorCode2',
      'ErrorMessage8'
    ),
    UnprocessedQueryExecutionId.new(
      'QueryExecutionId6',
      'ErrorCode2',
      'ErrorMessage8'
    ),
    UnprocessedQueryExecutionId.new(
      'QueryExecutionId6',
      'ErrorCode2',
      'ErrorMessage8'
    )
  ]
)
```



