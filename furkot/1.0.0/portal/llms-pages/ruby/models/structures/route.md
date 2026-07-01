# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `distance` | `Integer` | Optional | route distance in meters |
| `duration` | `Integer` | Optional | route duration in seconds |
| `mode` | [`ModeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/models/enumerations/mode.md) | Optional | travel mode |
| `polyline` | `String` | Optional | route path compatible with Google polyline encoding algorithm |


# Example

```ruby
route = Route.new(
  134,
  168,
  ModeEnum::CAR,
  'polyline0'
)
```



