# Notebook Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRk5vdGVib29rU2Vzc2lvblN1bW1hcnk

Contains the notebook session ID and notebook session creation time.

*This model accepts additional fields of type Object.*


# Class Name

`NotebookSessionSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `creation_time` | `DateTime` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
notebook_session_summary = NotebookSessionSummary.new(
  session_id: 'SessionId2',
  creation_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



