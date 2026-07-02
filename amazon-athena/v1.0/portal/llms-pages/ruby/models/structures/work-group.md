# Work Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRldvcmtHcm91cA

A workgroup, which contains a name, description, creation time, state, and other configuration, listed under <a>WorkGroup$Configuration</a>. Each workgroup enables you to isolate queries for you or your group of users from other queries in the same account, to configure the query results location and the encryption configuration (known as workgroup settings), to enable sending query metrics to Amazon CloudWatch, and to establish per-query data usage control limits for all queries in a workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.


# Class Name

`WorkGroup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state` | [`WorkGroupState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/work-group-state-3.md) | Optional | - |
| `configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/configuration.md) | Optional | - |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `creation_time` | `DateTime` | Optional | - |


# Example

```ruby
work_group = WorkGroup.new(
  'Name6',
  WorkGroupState3Enum::ENABLED,
  Configuration.new(
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
  ),
  'Description0',
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z')
)
```



