# Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRk5ldHdvcms


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


# Example

```ruby
network = Network.new(
  '2016-01-30T23:50:00+00:00',
  4711,
  '10.0.0.0/16',
  { 'key1' => 'val1', 'key2' => 'val2' },
  'mynet',
  Protection11.new(
    false
  ),
  [
    Route.new(
      '10.100.1.0/24',
      '10.0.1.1'
    )
  ],
  [
    42
  ],
  [
    Subnet.new(
      '10.0.0.1',
      'eu-central',
      Type42Enum::CLOUD,
      '10.0.1.0/24'
    )
  ],
  [
    42
  ]
)
```



