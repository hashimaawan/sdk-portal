# Notebook Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRk5vdGVib29rU2Vzc2lvblN1bW1hcnk

Contains the notebook session ID and notebook session creation time.


# Class Name

`NotebookSessionSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `creation_time` | `DateTime` | Optional | - |


# Example

```ruby
notebook_session_summary = NotebookSessionSummary.new(
  'SessionId2',
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z')
)
```



