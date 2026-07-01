# Location 16

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvY2F0aW9uMTY

Location of the Volume. Volume can only be attached to Servers in the same Location.

*This model accepts additional fields of type Object.*


# Class Name

`Location16`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `String` | Required | City the Location is closest to |
| `country` | `String` | Required | ISO 3166-1 alpha-2 code of the country the Location resides in |
| `description` | `String` | Required | Description of the Location |
| `id` | `Float` | Required | ID of the Location |
| `latitude` | `Float` | Required | Latitude of the city closest to the Location |
| `longitude` | `Float` | Required | Longitude of the city closest to the Location |
| `name` | `String` | Required | Unique identifier of the Location |
| `network_zone` | `String` | Required | Name of network zone this Location resides in |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
location16 = Location16.new(
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
)
```



