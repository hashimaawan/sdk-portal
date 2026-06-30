# Primary I Ps Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlByaW1hcnlJUHNSZXNwb25zZQ


# Class Name

`PrimaryIPsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `primary_ips` | [`Array[PrimaryIP1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/primary-ip-1.md) | Required | - |


# Example

```ruby
primary_i_ps_response = PrimaryIPsResponse.new(
  [
    PrimaryIP1.new(
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
        'key0': 'labels2',
        'key1': 'labels3',
        'key2': 'labels4'
      },
      'my-resource',
      Protection.new(
        false
      ),
      Type50Enum::IPV4
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



