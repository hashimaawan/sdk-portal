# Work Group Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb24

The configuration of the workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query and calculation results, whether the Amazon CloudWatch Metrics are enabled for the workgroup and whether workgroup settings override query settings, and the data usage limits for the amount of data scanned per query or per workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.

*This model accepts additional fields of type Object.*


# Class Name

`WorkGroupConfiguration`


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
work_group_configuration = WorkGroupConfiguration.new(
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



