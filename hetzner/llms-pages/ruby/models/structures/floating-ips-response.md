# Floating Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floating_ips` | [`Array[FloatingIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/floating-ip.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/meta.md) | Optional | - |


# Example

```ruby
floating_ips_response = FloatingIpsResponse.new(
  [
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
        'key0': 'labels2'
      },
      'my-resource',
      Protection.new(
        false
      ),
      42,
      Type16Enum::IPV4
    )
  ],
  Meta.new(
    Pagination.new(
      77.7,
      209.18,
      17.58,
      13.34,
      50.02,
      206.64
    )
  )
)
```



