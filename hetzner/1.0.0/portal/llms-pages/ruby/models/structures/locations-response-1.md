# Locations Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`LocationsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/location.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
locations_response1 = LocationsResponse1.new(
  location: Location.new(
    city: 'Falkenstein',
    country: 'DE',
    description: 'Falkenstein DC Park 1',
    id: 1,
    latitude: 50.47612,
    longitude: 12.370071,
    name: 'fsn1',
    network_zone: 'eu-central',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



