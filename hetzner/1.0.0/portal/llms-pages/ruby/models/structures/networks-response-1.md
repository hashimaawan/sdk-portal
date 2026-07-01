# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | [`Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/network.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
networks_response1 = NetworksResponse1.new(
  network: Network.new(
    created: 'created4',
    id: 78,
    ip_range: 'ip_range6',
    labels: { 'key1' => 'val1', 'key2' => 'val2' },
    name: 'name4',
    protection: Protection11.new(
      delete: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    routes: [
      Route.new(
        destination: 'destination8',
        gateway: 'gateway6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Route.new(
        destination: 'destination8',
        gateway: 'gateway6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Route.new(
        destination: 'destination8',
        gateway: 'gateway6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    servers: [
      93
    ],
    subnets: [
      Subnet.new(
        gateway: 'gateway4',
        network_zone: 'network_zone2',
        type: Type42::CLOUD,
        ip_range: 'ip_range6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    load_balancers: [
      208
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



