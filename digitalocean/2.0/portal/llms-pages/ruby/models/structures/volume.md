# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `String` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. |
| `description` | `String` | Optional | An optional free-form text field to describe a block storage volume. |
| `droplet_ids` | `Array[Integer]` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. |
| `id` | `String` | Optional, Read-only | The unique identifier for the block storage volume. |
| `name` | `String` | Optional | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. |
| `size_gigabytes` | `Integer` | Optional | The size of the block storage volume in GiB (1024^3). |
| `tags` | `Array[String]` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `filesystem_label` | `String` | Optional | The label currently applied to the filesystem. |
| `filesystem_type` | `String` | Optional | The type of filesystem currently in-use on the volume. |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/region.md) | Optional, Read-only | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
volume = Volume.new(
  created_at: '2020-03-02T17:00:49Z',
  description: 'Block store for examples',
  droplet_ids: [],
  id: '506f78a4-e098-11e5-ad9f-000f53306ae1',
  name: 'example',
  size_gigabytes: 10,
  tags: [
    'base-image',
    'prod'
  ],
  filesystem_label: 'example',
  filesystem_type: 'ext4',
  region: Region.new(
    available: true,
    features: [
      'private_networking',
      'backups',
      'ipv6',
      'metadata'
    ],
    name: 'New York 1',
    sizes: [
      's-1vcpu-1gb',
      's-1vcpu-2gb',
      's-1vcpu-3gb',
      's-2vcpu-2gb',
      's-3vcpu-1gb',
      's-2vcpu-4gb',
      's-4vcpu-8gb',
      's-6vcpu-16gb',
      's-8vcpu-32gb',
      's-12vcpu-48gb',
      's-16vcpu-64gb',
      's-20vcpu-96gb',
      's-24vcpu-128gb',
      's-32vcpu-192gb'
    ],
    slug: 'nyc1'
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



