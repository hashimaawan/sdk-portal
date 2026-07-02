# Query Execution 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uMQ

*This model accepts additional fields of type Object.*


# Class Name

`QueryExecution1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `query` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `statement_type` | [`StatementType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/statement-type-1.md) | Optional | - |
| `result_configuration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-configuration-1.md) | Optional | - |
| `result_reuse_configuration` | [`ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-reuse-configuration-1.md) | Optional | - |
| `query_execution_context` | [`QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-execution-context-1.md) | Optional | - |
| `status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status.md) | Optional | - |
| `statistics` | [`Statistics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/statistics.md) | Optional | - |
| `work_group` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-version-1.md) | Optional | - |
| `execution_parameters` | `Array[String]` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `substatement_type` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
query_execution1 = QueryExecution1.new(
  query_execution_id: 'QueryExecutionId0',
  query: 'Query6',
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
```



