# Time Interval Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlRpbWVJbnRlcnZhbE9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`TimeIntervalObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `start` | `Float` | Optional | The starting point (in seconds) of the time interval. |
| `duration` | `Float` | Optional | The duration (in seconds) of the time interval. |
| `confidence` | `Float` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the interval.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
time_interval_object = TimeIntervalObject.new(
  start: 0.49567,
  duration: 2.18749,
  confidence: 0.925,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



