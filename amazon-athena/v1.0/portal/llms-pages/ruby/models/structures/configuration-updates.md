# Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb25VcGRhdGVz

*This model accepts additional fields of type Object.*


# Class Name

`ConfigurationUpdates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enforce_work_group_configuration` | `TrueClass \| FalseClass` | Optional | - |
| `result_configuration_updates` | [`ResultConfigurationUpdates2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-configuration-updates-2.md) | Optional | - |
| `publish_cloud_watch_metrics_enabled` | `TrueClass \| FalseClass` | Optional | - |
| `bytes_scanned_cutoff_per_query` | `Integer` | Optional | **Constraints**: `>= 10000000` |
| `remove_bytes_scanned_cutoff_per_query` | `TrueClass \| FalseClass` | Optional | - |
| `requester_pays_enabled` | `TrueClass \| FalseClass` | Optional | - |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-version-1.md) | Optional | - |
| `remove_customer_content_encryption_configuration` | `TrueClass \| FalseClass` | Optional | - |
| `additional_configuration` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `execution_role` | `String` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `customer_content_encryption_configuration` | [`CustomerContentEncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/customer-content-encryption-configuration.md) | Optional | Specifies the KMS key that is used to encrypt the user's data stores in Athena. |
| `enable_minimum_encryption_configuration` | `TrueClass \| FalseClass` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
configuration_updates = ConfigurationUpdates.new(
  enforce_work_group_configuration: false,
  result_configuration_updates: ResultConfigurationUpdates2.new(
    output_location: 'OutputLocation0',
    remove_output_location: false,
    encryption_configuration: EncryptionConfiguration2.new(
      encryption_option: EncryptionOption1::SSE_S3,
      kms_key: 'KmsKey6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    remove_encryption_configuration: false,
    expected_bucket_owner: 'ExpectedBucketOwner0',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  publish_cloud_watch_metrics_enabled: false,
  bytes_scanned_cutoff_per_query: 10000000,
  remove_bytes_scanned_cutoff_per_query: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



