# V2 Tags Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2TagsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tags` | [`Array[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/tag.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_tags_response = V2TagsResponse.new(
  meta: Meta.new(
    total: 1,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  tags: [
    Tag.new(
      name: 'extra-awesome',
      resources: Resources2.new(
        count: 5,
        last_tagged_uri: 'https://api.digitalocean.com/v2/images/7555620',
        databases: Databases.new(
          count: 1,
          last_tagged_uri: 'https://api.digitalocean.com/v2/databases/b92438f6-ba03-416c-b642-e9236db91976',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        droplets: Databases.new(
          count: 1,
          last_tagged_uri: 'https://api.digitalocean.com/v2/droplets/3164444',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        imgages: Databases.new(
          count: 158,
          last_tagged_uri: 'last_tagged_uri4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        volume_snapshots: Databases.new(
          count: 1,
          last_tagged_uri: 'https://api.digitalocean.com/v2/snapshots/1f6f46e8-6b60-11e9-be4e-0a58ac144519'
        ),
        volumes: Databases.new(
          count: 1,
          last_tagged_uri: 'https://api.digitalocean.com/v2/volumes/3d80cb72-342b-4aaa-b92e-4e4abb24a933'
        ),
        additional_properties: {
          'images' => JSON.parse('{"count":1,"last_tagged_uri":"https://api.digitalocean.com/v2/images/7555620"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  links: Links.new(
    pages: Pages.new(
      last: 'last6',
      mnext: 'next2',
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



