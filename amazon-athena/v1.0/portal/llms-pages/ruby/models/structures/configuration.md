# Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb24

*This model accepts additional fields of type Object.*


# Class Name

`Configuration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `result_configuration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-configuration-1.md) | Optional | - |
| `enforce_work_group_configuration` | `TrueClass \| FalseClass` | Optional | - |
| `publish_cloud_watch_metrics_enabled` | `TrueClass \| FalseClass` | Optional | - |
| `bytes_scanned_cutoff_per_query` | `Integer` | Optional | **Constraints**: `>= 10000000` |
| `requester_pays_enabled` | `TrueClass \| FalseClass` | Optional | - |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-version-1.md) | Optional | - |
| `additional_configuration` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `execution_role` | `String` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `customer_content_encryption_configuration` | [`CustomerContentEncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/customer-content-encryption-configuration-2.md) | Optional | - |
| `enable_minimum_encryption_configuration` | `TrueClass \| FalseClass` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
configuration = Configuration.new(
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
  enforce_work_group_configuration: false,
  publish_cloud_watch_metrics_enabled: false,
  bytes_scanned_cutoff_per_query: 10000000,
  requester_pays_enabled: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



