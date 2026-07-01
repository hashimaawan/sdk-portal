# Step

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0ZXA


# Class Name

`Step`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address` | `String` | Optional | address of the stop |
| `arrival` | `DateTime` | Optional | arrival at the stop in its local timezone as YYYY-MM-DDThh:mm |
| `coordinates` | [`Coordinates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/models/structures/coordinates.md) | Optional | geographical coordinates of the stop |
| `departure` | `DateTime` | Optional | departure from the stop in its local timezone as YYYY-MM-DDThh:mm |
| `name` | `String` | Optional | name of the stop |
| `nights` | `Integer` | Optional | number of nights |
| `passthru` | `TrueClass \| FalseClass` | Optional | true for pass-through points anchoring route |
| `route` | [`Route`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/models/structures/route.md) | Optional | route leading to the stop |
| `url` | `String` | Optional | url of the page with more information about the stop |


# Example

```ruby
step = Step.new(
  'address4',
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  Coordinates.new(
    182.98,
    16.08
  ),
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  'name8',
  nil,
  nil,
  Route.new(
    nil,
    nil,
    envrr
  )
)
```



