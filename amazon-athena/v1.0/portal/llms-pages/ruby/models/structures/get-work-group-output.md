# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA


# Class Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | [`WorkGroup2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/work-group-2.md) | Optional | - |


# Example

```ruby
get_work_group_output = GetWorkGroupOutput.new(
  WorkGroup2.new(
    'Name2',
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
    'Description4',
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z')
  )
)
```



