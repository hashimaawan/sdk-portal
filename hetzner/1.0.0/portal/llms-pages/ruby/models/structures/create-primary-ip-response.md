# Create Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlc3BvbnNl


# Class Name

`CreatePrimaryIPResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Optional | - |
| `primary_ip` | [`PrimaryIP1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/primary-ip-1.md) | Required | - |


# Example

```ruby
create_primary_ip_response = CreatePrimaryIPResponse.new(
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
      'key1': 'labels1'
    },
    'my-resource',
    Protection.new(
      false
    ),
    Type50Enum::IPV4
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



