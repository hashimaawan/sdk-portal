# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaW1hcnlJUDE


# Class Name

`PrimaryIP1`


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
| `type` | [`Type50Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-50.md) | Required | Type of the Primary IP |


# Example

```ruby
primary_ip1 = PrimaryIP1.new(
  17,
  'server',
  true,
  false,
  '2016-01-30T23:55:00+00:00',
  Datacenter2.new(
    'Falkenstein DC Park 8',
    42,
    Location.new(
      'Falkenstein',
      'DE',
      'Falkenstein DC Park 1',
      1,
      50.47612,
      12.370071,
      'fsn1',
      'eu-central'
    ),
    'fsn1-dc8',
    ServerTypes.new(
      [
        1,
        2,
        3
      ],
      [
        1,
        2,
        3
      ],
      [
        1,
        2,
        3
      ]
    )
  ),
  [
    DnsPtr.new(
      'server.example.com',
      '2001:db8::1'
    )
  ],
  42,
  '131.232.99.1',
  {
    'key0': 'labels6',
    'key1': 'labels7',
    'key2': 'labels8'
  },
  'my-resource',
  Protection.new(
    false
  ),
  Type50Enum::IPV4
)
```



