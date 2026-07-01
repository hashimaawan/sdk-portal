# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop

*This model accepts additional fields of type Object.*


# Class Name

`Coordinates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lat` | `Float` | Optional | latitude |
| `lon` | `Float` | Optional | longitude |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
coordinates = Coordinates.new(
  lat: 182.98,
  lon: 16.08,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



