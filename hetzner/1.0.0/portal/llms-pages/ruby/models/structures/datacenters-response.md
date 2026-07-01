# Datacenters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`DatacentersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datacenters` | [`Array[Datacenter]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/datacenter.md) | Required | - |
| `recommendation` | `Float` | Required | The Datacenter which is recommended to be used to create new Servers. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
datacenters_response = DatacentersResponse.new(
  datacenters: [
    Datacenter.new(
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
  ],
  recommendation: 1,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



