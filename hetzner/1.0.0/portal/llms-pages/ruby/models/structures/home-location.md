# Home Location

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkhvbWVMb2NhdGlvbg

Location the Floating IP was created in. Routing is optimized for this Location.


# Class Name

`HomeLocation`


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


# Example

```ruby
home_location = HomeLocation.new(
  'Falkenstein',
  'DE',
  'Falkenstein DC Park 1',
  1,
  50.47612,
  12.370071,
  'fsn1',
  'eu-central'
)
```



