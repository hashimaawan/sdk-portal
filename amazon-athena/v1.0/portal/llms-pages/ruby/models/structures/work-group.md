# Work Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRldvcmtHcm91cA

A workgroup, which contains a name, description, creation time, state, and other configuration, listed under <a>WorkGroup$Configuration</a>. Each workgroup enables you to isolate queries for you or your group of users from other queries in the same account, to configure the query results location and the encryption configuration (known as workgroup settings), to enable sending query metrics to Amazon CloudWatch, and to establish per-query data usage control limits for all queries in a workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.

*This model accepts additional fields of type Object.*


# Class Name

`WorkGroup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state` | [`WorkGroupState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/work-group-state-3.md) | Optional | - |
| `configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/configuration.md) | Optional | - |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `creation_time` | `DateTime` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
work_group = WorkGroup.new(
  name: 'Name6',
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
  description: 'Description0',
  creation_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



