# List Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1Jlc3BvbnNl


# Class Name

`ListSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `sessions` | [`Array[SessionSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/session-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |


# Example

```ruby
list_sessions_response = ListSessionsResponse.new(
  'NextToken2',
  [
    SessionSummary.new(
      'SessionId6',
      'Description4',
      EngineVersion1.new(
        'SelectedEngineVersion4',
        'EffectiveEngineVersion6'
      ),
      'NotebookVersion6',
      Status3.new(
        DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        SessionState1Enum::TERMINATING
      )
    )
  ]
)
```



