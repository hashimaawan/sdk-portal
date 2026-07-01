# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
images_response1 = ImagesResponse1.new(
  image: Image.new(
    bound_to: 186,
    created: 'created6',
    created_from: CreatedFrom.new(
      id: 60,
      name: 'name6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    deleted: 'deleted4',
    deprecated: 'deprecated8',
    description: 'description6',
    disk_size: 244.18,
    id: 128,
    image_size: 141.34,
    labels: {
      'key0' => 'labels4'
    },
    name: 'name6',
    os_flavor: OsFlavor::DEBIAN,
    os_version: 'os_version4',
    protection: Protection.new(
      delete: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    status: Status24::UNAVAILABLE,
    type: Type22::APP,
    rapid_deploy: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



