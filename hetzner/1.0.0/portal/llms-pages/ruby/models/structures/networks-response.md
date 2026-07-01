# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `networks` | [`Array[Network]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/network.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
networks_response = NetworksResponse.new(
  networks: [
    Network.new(
      created: '2016-01-30T23:50:00+00:00',
      id: 4711,
      ip_range: '10.0.0.0/16',
      labels: { 'key1' => 'val1', 'key2' => 'val2' },
      name: 'mynet',
      protection: Protection11.new(
        delete: false,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      routes: [
        Route.new(
          destination: '10.100.1.0/24',
          gateway: '10.0.1.1',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      servers: [
        42
      ],
      subnets: [
        Subnet.new(
          gateway: '10.0.0.1',
          network_zone: 'eu-central',
          type: Type42::CLOUD,
          ip_range: '10.0.1.0/24',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      load_balancers: [
        42
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  meta: Meta.new(
    pagination: Pagination.new(
      last_page: 77.7,
      next_page: 209.18,
      page: 17.58,
      per_page: 13.34,
      previous_page: 50.02,
      total_entries: 206.64,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



