# V2 Volumes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2VolumesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `String` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. |
| `description` | `String` | Optional | An optional free-form text field to describe a block storage volume. |
| `droplet_ids` | `Array[Integer]` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. |
| `id` | `String` | Optional, Read-only | The unique identifier for the block storage volume. |
| `name` | `String` | Required | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. |
| `size_gigabytes` | `Integer` | Required | The size of the block storage volume in GiB (1024^3). |
| `tags` | `Array[String]` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `snapshot_id` | `String` | Optional | The unique identifier for the volume snapshot from which to create the volume. |
| `filesystem_type` | `String` | Optional | The name of the filesystem type to be used on the volume. When provided, the volume will automatically be formatted to the specified filesystem type. Currently, the available options are `ext4` and `xfs`. Pre-formatted volumes are automatically mounted when attached to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS Droplets created on or after April 26, 2018. Attaching pre-formatted volumes to other Droplets is not recommended. |
| `filesystem_label` | `String` | Optional | **Constraints**: *Maximum Length*: `16` |
| `region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_volumes_request = V2VolumesRequest.new(
  name: 'example',
  size_gigabytes: 10,
  region: Region2::NYC3,
  created_at: '2020-03-02T17:00:49Z',
  description: 'Block store for examples',
  droplet_ids: [],
  id: '506f78a4-e098-11e5-ad9f-000f53306ae1',
  tags: [
    'base-image',
    'prod'
  ],
  snapshot_id: 'b0798135-fb76-11eb-946a-0a58ac146f33',
  filesystem_type: 'ext4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



