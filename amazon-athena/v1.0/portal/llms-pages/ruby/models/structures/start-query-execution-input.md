# Start Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25JbnB1dA

*This model accepts additional fields of type Object.*


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
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
start_query_execution_input = StartQueryExecutionInput.new(
  query_string: 'QueryString6',
  client_request_token: 'ClientRequestToken8',
  query_execution_context: QueryExecutionContext1.new(
    database: 'Database4',
    catalog: 'Catalog0',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
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
  work_group: 'WorkGroup6',
  execution_parameters: [
    'ExecutionParameters8',
    'ExecutionParameters7'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



