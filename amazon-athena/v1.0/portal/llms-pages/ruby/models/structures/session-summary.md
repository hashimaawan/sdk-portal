# Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlc3Npb25TdW1tYXJ5

Contains summary information about a session.

*This model accepts additional fields of type Object.*


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
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
session_summary = SessionSummary.new(
  session_id: 'SessionId8',
  description: 'Description6',
  engine_version: EngineVersion1.new(
    selected_engine_version: 'SelectedEngineVersion4',
    effective_engine_version: 'EffectiveEngineVersion6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  notebook_version: 'NotebookVersion4',
  status: Status3.new(
    start_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    last_modified_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    end_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    idle_since_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    state: SessionState1::TERMINATING,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



