# Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlc3Npb25TdW1tYXJ5

Contains summary information about a session.


# Class Name

`SessionSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-version-1.md) | Optional | - |
| `notebook_version` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status-3.md) | Optional | - |


# Example

```ruby
session_summary = SessionSummary.new(
  'SessionId8',
  'Description6',
  EngineVersion1.new(
    'SelectedEngineVersion4',
    'EffectiveEngineVersion6'
  ),
  'NotebookVersion4',
  Status3.new(
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    SessionState1Enum::TERMINATING
  )
)
```



