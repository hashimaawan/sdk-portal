# Volumes Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMg


# Class Name

`VolumesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/volume-1.md) | Required | - |


# Example

```ruby
volumes_response2 = VolumesResponse2.new(
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



