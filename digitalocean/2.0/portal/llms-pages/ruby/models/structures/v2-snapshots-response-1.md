# V2 Snapshots Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2SnapshotsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshot` | [`Snapshot`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/snapshot.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_snapshots_response1 = V2SnapshotsResponse1.new(
  snapshot: Snapshot.new(
    id: 'id8',
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    min_disk_size: 36,
    name: 'name8',
    regions: [
      'regions3',
      'regions4',
      'regions5'
    ],
    size_gigabytes: 140.04,
    resource_id: 'resource_id4',
    resource_type: ResourceType1::DROPLET,
    tags: [
      'tags3'
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



