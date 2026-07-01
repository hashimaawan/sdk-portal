# Datacenter 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGFjZW50ZXI2

Datacenter this Resource is located at

*This model accepts additional fields of type Object.*


# Class Name

`Datacenter6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Required | Description of the Datacenter |
| `id` | `Integer` | Required | ID of the Resource |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/location.md) | Required | - |
| `name` | `String` | Required | Unique identifier of the Datacenter |
| `server_types` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-types.md) | Required | The Server types the Datacenter can handle |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
datacenter6 = Datacenter6.new(
  description: 'Falkenstein DC Park 8',
  id: 42,
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
  name: 'fsn1-dc8',
  server_types: ServerTypes.new(
    available: [
      1,
      2,
      3
    ],
    available_for_migration: [
      1,
      2,
      3
    ],
    supported: [
      1,
      2,
      3
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



