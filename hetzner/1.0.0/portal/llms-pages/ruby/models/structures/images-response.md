# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `images` | [`Array[Image]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/image.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
images_response = ImagesResponse.new(
  images: [
    Image.new(
      bound_to: nil,
      created: '2016-01-30T23:55:00+00:00',
      created_from: CreatedFrom.new(
        id: 1,
        name: 'Server',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      deleted: nil,
      deprecated: '2018-02-28T00:00:00+00:00',
      description: 'Ubuntu 20.04 Standard 64 bit',
      disk_size: 10,
      id: 42,
      image_size: 2.3,
      labels: {
        'key0' => 'labels0',
        'key1' => 'labels1'
      },
      name: 'ubuntu-20.04',
      os_flavor: OsFlavor::UBUNTU,
      os_version: '20.04',
      protection: Protection.new(
        delete: false,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      status: Status24::AVAILABLE,
      type: Type22::SNAPSHOT,
      rapid_deploy: false,
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



