# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0


# Class Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/configuration.md) | Optional | - |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `tags` | [`Array[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/tag.md) | Optional | - |


# Example

```ruby
create_work_group_input = CreateWorkGroupInput.new(
  'Name8',
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
  'Description8',
  [
    Tag.new(
      'Key0',
      'Value6'
    )
  ]
)
```



