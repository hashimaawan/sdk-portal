# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution` | [`QueryExecution1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-execution-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_query_execution_output = GetQueryExecutionOutput.new(
  query_execution: QueryExecution1.new(
    query_execution_id: 'QueryExecutionId0',
    query: 'Query6',
    statement_type: StatementType1::DDL,
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
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



