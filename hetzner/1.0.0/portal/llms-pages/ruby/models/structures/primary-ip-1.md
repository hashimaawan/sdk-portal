# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaW1hcnlJUDE

*This model accepts additional fields of type Object.*


# Class Name

`PrimaryIp1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee_id` | `Integer` | Required | ID of the resource the Primary IP is assigned to, null if it is not assigned at all |
| `assignee_type` | `String` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `'server'` |
| `auto_delete` | `TrueClass \| FalseClass` | Required | Delete this Primary IP when the resource it is assigned to is deleted |
| `blocked` | `TrueClass \| FalseClass` | Required | Whether the IP is blocked |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `datacenter` | [`Datacenter2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/datacenter-2.md) | Required | Datacenter this Primary IP is located at |
| `dns_ptr` | [`Array[DnsPtr]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `id` | `Integer` | Required | ID of the Resource |
| `ip` | `String` | Required | IP address |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `type` | [`Type50`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-50.md) | Required | Type of the Primary IP |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
primary_ip1 = PrimaryIp1.new(
  assignee_id: 17,
  assignee_type: 'server',
  auto_delete: true,
  blocked: false,
  created: '2016-01-30T23:55:00+00:00',
  datacenter: Datacenter2.new(
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
  ),
  dns_ptr: [
    DnsPtr.new(
      dns_ptr: 'server.example.com',
      ip: '2001:db8::1',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  id: 42,
  ip: '131.232.99.1',
  labels: {
    'key0' => 'labels6',
    'key1' => 'labels7',
    'key2' => 'labels8'
  },
  name: 'my-resource',
  protection: Protection.new(
    delete: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  type: Type50::IPV4,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



