# Update Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZVdvcmtHcm91cElucHV0


# Class Name

`UpdateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `configuration_updates` | [`ConfigurationUpdates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/configuration-updates.md) | Optional | - |
| `state` | [`WorkGroupState2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/work-group-state-2.md) | Optional | - |


# Example

```ruby
update_work_group_input = UpdateWorkGroupInput.new(
  'WorkGroup0',
  'Description8',
  ConfigurationUpdates.new(
    false,
    ResultConfigurationUpdates2.new(
      'OutputLocation0',
      false,
      EncryptionConfiguration2.new(
        EncryptionOption1Enum::SSE_S3,
        'KmsKey6'
      ),
      false,
      'ExpectedBucketOwner0',
      nil,
      AclConfiguration1.new(
        envrr
      )
    ),
    false,
    10000000,
    false,
    nil,
    EngineVersion1.new,
    nil,
    nil,
    nil,
    CustomerContentEncryptionConfiguration.new
  ),
  WorkGroupState2Enum::ENABLED
)
```



