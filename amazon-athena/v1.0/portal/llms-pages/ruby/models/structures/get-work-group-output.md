# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA

*This model accepts additional fields of type Object.*


# Class Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | [`WorkGroup2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/work-group-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_work_group_output = GetWorkGroupOutput.new(
  work_group: WorkGroup2.new(
    name: 'Name2',
    state: WorkGroupState3::ENABLED,
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
    description: 'Description4',
    creation_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



