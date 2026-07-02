# V2 Tags Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2TagsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tag` | [`Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/tag.md) | Optional | A tag is a label that can be applied to a resource (currently Droplets, Images, Volumes, Volume Snapshots, and Database clusters) in order to better organize or facilitate the lookups and actions on it.<br>Tags have two attributes: a user defined `name` attribute and an embedded `resources` attribute with information about resources that have been tagged. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_tags_response1 = V2TagsResponse1.new(
  tag: Tag.new(
    name: 'extra-awesome',
    resources: Resources2.new(
      count: 0,
      last_tagged_uri: 'last_tagged_uri6',
      databases: Databases.new(
        count: 0,
        last_tagged_uri: 'last_tagged_uri2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      droplets: Databases.new(
        count: 0,
        last_tagged_uri: 'last_tagged_uri6',
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
        count: 0
      ),
      volumes: Databases.new(
        count: 0
      ),
      additional_properties: {
        'images' => JSON.parse('{"count":0}')
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



