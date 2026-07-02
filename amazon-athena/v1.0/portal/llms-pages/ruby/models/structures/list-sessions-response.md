# List Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1Jlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`ListSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `sessions` | [`Array[SessionSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/session-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_sessions_response = ListSessionsResponse.new(
  next_token: 'NextToken2',
  sessions: [
    SessionSummary.new(
      session_id: 'SessionId6',
      description: 'Description4',
      engine_version: EngineVersion1.new(
        selected_engine_version: 'SelectedEngineVersion4',
        effective_engine_version: 'EffectiveEngineVersion6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      notebook_version: 'NotebookVersion6',
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
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



