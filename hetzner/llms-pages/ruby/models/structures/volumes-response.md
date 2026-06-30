# Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNl


# Class Name

`VolumesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `volumes` | [`Array[Volume1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/volume-1.md) | Required | - |


# Example

```ruby
volumes_response = VolumesResponse.new(
  [
    Volume1.new(
      '2016-01-30T23:55:00+00:00',
      'xfs',
      42,
      {
        'key0': 'labels4'
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



