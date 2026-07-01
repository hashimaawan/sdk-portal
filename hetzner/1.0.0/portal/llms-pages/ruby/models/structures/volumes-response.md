# Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`VolumesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `volumes` | [`Array[Volume1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/volume-1.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
volumes_response = VolumesResponse.new(
  volumes: [
    Volume1.new(
      created: '2016-01-30T23:55:00+00:00',
      format: 'xfs',
      id: 42,
      labels: {
        'key0' => 'labels4'
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
  ],
  meta: Meta.new(
    pagination: Pagination.new(
      last_page: 77.7,
      next_page: 209.18,
      page: 17.58,
      per_page: 13.34,
      previous_page: 50.02,
      total_entries: 206.64,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



