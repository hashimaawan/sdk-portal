# Trip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlRyaXA

*This model accepts additional fields of type Object.*


# Class Name

`Trip`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mbegin` | `DateTime` | Optional | begin of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `description` | `String` | Optional | description of the trip (truncated to 200 characters) |
| `mend` | `DateTime` | Optional | end of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `id` | `String` | Optional | Unique ID of the trip |
| `name` | `String` | Optional | name of the trip |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
trip = Trip.new(
  mbegin: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  description: 'description8',
  mend: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  id: 'id8',
  name: 'name8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



