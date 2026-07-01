# Volume 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZTE

*This model accepts additional fields of type Object.*


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
| `location` | [`Location16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/location-16.md) | Required | Location of the Volume. Volume can only be attached to Servers in the same Location. |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `server` | `Integer` | Required | ID of the Server the Volume is attached to, null if it is not attached at all |
| `size` | `Float` | Required | Size in GB of the Volume |
| `status` | [`Status113`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/status-113.md) | Required | Current status of the Volume |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
volume1 = Volume1.new(
  created: '2016-01-30T23:55:00+00:00',
  format: 'xfs',
  id: 42,
  labels: {
    'key0' => 'labels8'
  },
  linux_device: '/dev/disk/by-id/scsi-0HC_Volume_4711',
  location: Location16.new(
    city: 'Falkenstein',
    country: 'DE',
    description: 'Falkenstein DC Park 1',
    id: 1,
    latitude: 50.47612,
    longitude: 12.370071,
    name: 'fsn1',
    network_zone: 'eu-central',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  name: 'my-resource',
  protection: Protection.new(
    delete: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  server: 12,
  size: 42,
  status: Status113::AVAILABLE,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



