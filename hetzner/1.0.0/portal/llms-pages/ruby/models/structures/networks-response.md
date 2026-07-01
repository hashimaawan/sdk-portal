# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ


# Class Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `networks` | [`Array[Network]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/network.md) | Required | - |


# Example

```ruby
networks_response = NetworksResponse.new(
  [
    Network.new(
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



