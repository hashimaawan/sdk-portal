# Update Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type Object.*


# Class Name

`UpdateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `configuration_updates` | [`ConfigurationUpdates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/configuration-updates.md) | Optional | - |
| `state` | [`WorkGroupState2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/work-group-state-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
update_work_group_input = UpdateWorkGroupInput.new(
  work_group: 'WorkGroup0',
  description: 'Description8',
  configuration_updates: ConfigurationUpdates.new(
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
  ),
  state: WorkGroupState2::ENABLED,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



