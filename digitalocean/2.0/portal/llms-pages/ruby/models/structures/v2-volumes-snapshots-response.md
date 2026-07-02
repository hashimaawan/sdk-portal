# V2 Volumes Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2VolumesSnapshotsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshot` | [`Snapshot`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/snapshot.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_volumes_snapshots_response = V2VolumesSnapshotsResponse.new(
  snapshot: Snapshot.new(
    id: '8fa70202-873f-11e6-8b68-000f533176b1',
    created_at: DateTimeHelper.from_rfc3339('2020-09-30T18:56:14Z'),
    min_disk_size: 10,
    name: 'big-data-snapshot1475261774',
    regions: [
      'nyc1'
    ],
    size_gigabytes: 10,
    resource_id: '82a48a18-873f-11e6-96bf-000f53315a41',
    resource_type: ResourceType1::VOLUME,
    tags: [
      'aninterestingtag'
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



