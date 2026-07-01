# Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRk5ldHdvcms

*This model accepts additional fields of type Object.*


# Class Name

`Network`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `String` | Required | Point in time when the Network was created (in ISO-8601 format) |
| `id` | `Integer` | Required | ID of the Network |
| `ip_range` | `String` | Required | IPv4 prefix of the whole Network |
| `labels` | `Object` | Required | User-defined labels (key-value pairs) |
| `load_balancers` | `Array[Integer]` | Optional | Array of IDs of Load Balancers attached to this Network |
| `name` | `String` | Required | Name of the Network |
| `protection` | [`Protection11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/protection-11.md) | Required | Protection configuration for the Network |
| `routes` | [`Array[Route]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/route.md) | Required | Array of routes set in this Network |
| `servers` | `Array[Integer]` | Required | Array of IDs of Servers attached to this Network |
| `subnets` | [`Array[Subnet]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/subnet.md) | Required | Array subnets allocated in this Network |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
network = Network.new(
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
```



