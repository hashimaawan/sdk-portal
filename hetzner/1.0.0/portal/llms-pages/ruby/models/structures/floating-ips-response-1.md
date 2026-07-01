# Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMQ


# Class Name

`FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Optional | - |
| `floating_ip` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/floating-ip.md) | Required | - |


# Example

```ruby
floating_ips_response1 = FloatingIpsResponse1.new(
  FloatingIp.new(
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
  ),
  Action.new(
    'command6',
    Error.new(
      'code2',
      'message4'
    ),
    'finished0',
    238,
    143.26,
    [
      Resource.new(
        198,
        'type0'
      ),
      Resource.new(
        198,
        'type0'
      ),
      Resource.new(
        198,
        'type0'
      )
    ],
    'started8',
    StatusEnum::RUNNING
  )
)
```



