# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_executions` | [`Array[QueryExecution]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-execution.md) | Optional | - |
| `unprocessed_query_execution_ids` | [`Array[UnprocessedQueryExecutionId]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/unprocessed-query-execution-id.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
batch_get_query_execution_output = BatchGetQueryExecutionOutput.new(
  query_executions: [
    QueryExecution.new(
      query_execution_id: 'QueryExecutionId6',
      query: 'Query0',
      statement_type: StatementType1::UTILITY,
      result_configuration: ResultConfiguration1.new(
        output_location: 'OutputLocation0',
        encryption_configuration: EncryptionConfiguration2.new(
          encryption_option: EncryptionOption1::SSE_S3,
          kms_key: 'KmsKey6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        expected_bucket_owner: 'ExpectedBucketOwner0',
        acl_configuration: AclConfiguration1.new(
          s3_acl_option: S3AclOption1::BUCKET_OWNER_FULL_CONTROL,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      result_reuse_configuration: ResultReuseConfiguration1.new(
        result_reuse_by_age_configuration: ResultReuseByAgeConfiguration2.new(
          enabled: false,
          max_age_in_minutes: 26,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    QueryExecution.new(
      query_execution_id: 'QueryExecutionId6',
      query: 'Query0',
      statement_type: StatementType1::UTILITY,
      result_configuration: ResultConfiguration1.new(
        output_location: 'OutputLocation0',
        encryption_configuration: EncryptionConfiguration2.new(
          encryption_option: EncryptionOption1::SSE_S3,
          kms_key: 'KmsKey6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        expected_bucket_owner: 'ExpectedBucketOwner0',
        acl_configuration: AclConfiguration1.new(
          s3_acl_option: S3AclOption1::BUCKET_OWNER_FULL_CONTROL,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      result_reuse_configuration: ResultReuseConfiguration1.new(
        result_reuse_by_age_configuration: ResultReuseByAgeConfiguration2.new(
          enabled: false,
          max_age_in_minutes: 26,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  unprocessed_query_execution_ids: [
    UnprocessedQueryExecutionId.new(
      query_execution_id: 'QueryExecutionId6',
      error_code: 'ErrorCode2',
      error_message: 'ErrorMessage8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    UnprocessedQueryExecutionId.new(
      query_execution_id: 'QueryExecutionId6',
      error_code: 'ErrorCode2',
      error_message: 'ErrorMessage8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    UnprocessedQueryExecutionId.new(
      query_execution_id: 'QueryExecutionId6',
      error_code: 'ErrorCode2',
      error_message: 'ErrorMessage8',
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



