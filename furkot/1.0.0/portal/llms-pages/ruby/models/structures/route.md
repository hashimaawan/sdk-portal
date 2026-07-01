# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop

*This model accepts additional fields of type Object.*


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `distance` | `Integer` | Optional | route distance in meters |
| `duration` | `Integer` | Optional | route duration in seconds |
| `mode` | [`Mode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/models/enumerations/mode.md) | Optional | travel mode |
| `polyline` | `String` | Optional | route path compatible with Google polyline encoding algorithm |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
route = Route.new(
  distance: 134,
  duration: 168,
  mode: Mode::CAR,
  polyline: 'polyline0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



