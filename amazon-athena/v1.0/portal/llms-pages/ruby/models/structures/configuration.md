# Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb24


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


# Example

```ruby
configuration = Configuration.new(
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
  false,
  false,
  10000000,
  false,
  EngineVersion1.new,
  nil,
  nil,
  CustomerContentEncryptionConfiguration2.new
)
```



