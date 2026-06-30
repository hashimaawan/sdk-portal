# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | [`Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/network.md) | Optional | - |


# Example

```ruby
networks_response1 = NetworksResponse1.new(
  Network.new(
    'created4',
    78,
    'ip_range6',
    { 'key1' => 'val1', 'key2' => 'val2' },
    'name4',
    Protection11.new(
      false
    ),
    [
      Route.new(
        'destination8',
        'gateway6'
      ),
      Route.new(
        'destination8',
        'gateway6'
      ),
      Route.new(
        'destination8',
        'gateway6'
      )
    ],
    [
      93
    ],
    [
      Subnet.new(
        'gateway4',
        'network_zone2',
        Type42Enum::CLOUD,
        'ip_range6'
      )
    ],
    [
      208
    ]
  )
)
```



