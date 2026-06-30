# Volume 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZTE


# Class Name

`Volume1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `format` | `String` | Required | Filesystem of the Volume if formatted on creation, null if not formatted on creation |
| `id` | `Integer` | Required | ID of the Resource |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `linux_device` | `String` | Required | Device path on the file system for the Volume |
| `location` | [`Location16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/location-16.md) | Required | Location of the Volume. Volume can only be attached to Servers in the same Location. |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `server` | `Integer` | Required | ID of the Server the Volume is attached to, null if it is not attached at all |
| `size` | `Float` | Required | Size in GB of the Volume |
| `status` | [`Status113Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/status-113.md) | Required | Current status of the Volume |


# Example

```ruby
volume1 = Volume1.new(
  '2016-01-30T23:55:00+00:00',
  'xfs',
  42,
  {
    'key0': 'labels8'
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
```



