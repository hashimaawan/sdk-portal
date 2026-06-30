# Trip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/ruby/x-redirect/JTI0bSUyRlRyaXA


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


# Example

```ruby
trip = Trip.new(
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  'description8',
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  'id8',
  'name8'
)
```



