# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA

*This model accepts additional fields of type Object.*


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
| `type` | [`Type16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-16.md) | Required | Type of the Floating IP |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
floating_ip = FloatingIp.new(
  blocked: false,
  created: '2016-01-30T23:55:00+00:00',
  description: 'this describes my resource',
  dns_ptr: [
    DnsPtr.new(
      dns_ptr: 'server.example.com',
      ip: '2001:db8::1',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  home_location: HomeLocation.new(
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
  id: 42,
  ip: '131.232.99.1',
  labels: {
    'key0' => 'labels4',
    'key1' => 'labels3',
    'key2' => 'labels2'
  },
  name: 'my-resource',
  protection: Protection.new(
    delete: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  server: 42,
  type: Type16::IPV4,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



