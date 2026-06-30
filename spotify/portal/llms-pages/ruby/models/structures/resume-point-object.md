# Resume Point Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlJlc3VtZVBvaW50T2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`ResumePointObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fully_played` | `TrueClass \| FalseClass` | Optional | Whether or not the episode has been fully played by the user. |
| `resume_position_ms` | `Integer` | Optional | The user's most recent position in the episode in milliseconds. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
resume_point_object = ResumePointObject.new(
  fully_played: false,
  resume_position_ms: 36,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



