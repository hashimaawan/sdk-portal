# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0


# Class Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution` | [`QueryExecution1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-execution-1.md) | Optional | - |


# Example

```ruby
get_query_execution_output = GetQueryExecutionOutput.new(
  QueryExecution1.new(
    'QueryExecutionId0',
    'Query6',
    StatementType1Enum::DDL,
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
)
```



