# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type Object.*


# Class Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/configuration.md) | Optional | - |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `tags` | [`Array[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/tag.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_work_group_input = CreateWorkGroupInput.new(
  name: 'Name8',
  configuration: Configuration.new(
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
  ),
  description: 'Description8',
  tags: [
    Tag.new(
      key: 'Key0',
      value: 'Value6',
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



