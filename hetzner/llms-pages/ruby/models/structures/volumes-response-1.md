# Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMQ


# Class Name

`VolumesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action.md) | Required | - |
| `next_actions` | [`Array[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action.md) | Required | - |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/volume-1.md) | Required | - |


# Example

```ruby
volumes_response1 = VolumesResponse1.new(
  Action.new(
    'start_server',
    Error.new(
      'action_failed',
      'Action failed'
    ),
    '2016-01-30T23:55:00+00:00',
    42,
    100,
    [
      Resource.new(
        42,
        'server'
      )
    ],
    '2016-01-30T23:55:00+00:00',
    StatusEnum::RUNNING
  ),
  [
    Action.new(
      'start_server',
      Error.new(
        'action_failed',
        'Action failed'
      ),
      '2016-01-30T23:55:00+00:00',
      42,
      100,
      [
        Resource.new(
          42,
          'server'
        )
      ],
      '2016-01-30T23:55:00+00:00',
      StatusEnum::SUCCESS
    )
  ],
  Volume1.new(
    '2016-01-30T23:55:00+00:00',
    'xfs',
    42,
    {
      'key0': 'labels8',
      'key1': 'labels9',
      'key2': 'labels0'
    },
    '/dev/disk/by-id/scsi-0HC_Volume_4711',
    Location16.new(
      'Falkenstein',
      'DE',
      'Falkenstein DC Park 1',
      1,
      50.47612,
      12.370071,
      'fsn1',
      'eu-central'
    ),
    'my-resource',
    Protection.new(
      false
    ),
    12,
    42,
    Status113Enum::AVAILABLE
  )
)
```



