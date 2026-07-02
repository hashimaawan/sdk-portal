# Get Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXNwb25zZQ


# Class Name

`GetSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `work_group` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engine_version` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `engine_configuration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-configuration-1.md) | Optional | - |
| `notebook_version` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `session_configuration` | [`SessionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/session-configuration-2.md) | Optional | - |
| `status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status-3.md) | Optional | - |
| `statistics` | [`Statistics3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/statistics-3.md) | Optional | - |


# Example

```ruby
get_session_response = GetSessionResponse.new(
  'SessionId6',
  'Description4',
  'WorkGroup4',
  'EngineVersion8',
  EngineConfiguration1.new(
    94,
    1,
    1,
    AdditionalConfigs.new
  ),
  nil,
  SessionConfiguration2.new(
    nil,
    nil,
    nil,
    EncryptionConfiguration.new(
      envrr
    )
  ),
  Status3.new(
    DateTimeHelper.from_rfc3339(nil),
    DateTimeHelper.from_rfc3339(nil),
    DateTimeHelper.from_rfc3339(nil),
    DateTimeHelper.from_rfc3339(nil),
    envrr
  ),
  Statistics3.new
)
```



