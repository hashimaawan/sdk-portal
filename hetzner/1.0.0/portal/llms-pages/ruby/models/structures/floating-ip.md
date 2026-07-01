# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `TrueClass \| FalseClass` | Required | Whether the IP is blocked |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `description` | `String` | Required | Description of the Resource |
| `dns_ptr` | [`Array[DnsPtr]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `home_location` | [`HomeLocation`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/home-location.md) | Required | Location the Floating IP was created in. Routing is optimized for this Location. |
| `id` | `Integer` | Required | ID of the Resource |
| `ip` | `String` | Required | IP address |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `server` | `Integer` | Required | ID of the Server the Floating IP is assigned to, null if it is not assigned at all |
| `type` | [`Type16Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-16.md) | Required | Type of the Floating IP |


# Example

```ruby
floating_ip = FloatingIp.new(
  false,
  '2016-01-30T23:55:00+00:00',
  'this describes my resource',
  [
    DnsPtr.new(
      'server.example.com',
      '2001:db8::1'
    )
  ],
  HomeLocation.new(
    'Falkenstein',
    'DE',
    'Falkenstein DC Park 1',
    1,
    50.47612,
    12.370071,
    'fsn1',
    'eu-central'
  ),
  42,
  '131.232.99.1',
  {
    'key0': 'labels4',
    'key1': 'labels3',
    'key2': 'labels2'
  },
  'my-resource',
  Protection.new(
    false
  ),
  42,
  Type16Enum::IPV4
)
```



