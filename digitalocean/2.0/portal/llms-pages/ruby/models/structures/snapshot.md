# Snapshot

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlNuYXBzaG90

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Snapshot`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Required | The unique identifier for the snapshot. |
| `created_at` | `DateTime` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. |
| `min_disk_size` | `Integer` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. |
| `name` | `String` | Required | A human-readable name for the snapshot. |
| `regions` | `Array[String]` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. |
| `size_gigabytes` | `Float` | Required | The billable size of the snapshot in gigabytes. |
| `resource_id` | `String` | Required | The unique identifier for the resource that the snapshot originated from. |
| `resource_type` | [`ResourceType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/resource-type-1.md) | Required | The type of resource that the snapshot originated from. |
| `tags` | `Array[String]` | Required | An array of Tags the snapshot has been tagged with. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
snapshot = Snapshot.new(
  id: '6372321',
  created_at: DateTimeHelper.from_rfc3339('2020-07-28T16:47:44Z'),
  min_disk_size: 25,
  name: 'web-01-1595954862243',
  regions: [
    'nyc3',
    'sfo3'
  ],
  size_gigabytes: 2.34,
  resource_id: '200776916',
  resource_type: ResourceType1::DROPLET,
  tags: [
    'web',
    'env:prod'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



