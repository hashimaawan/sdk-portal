# Repository

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlcG9zaXRvcnk

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Repository`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `latest_tag` | [`LatestTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/latest-tag.md) | Optional | - |
| `name` | `String` | Optional | The name of the repository. |
| `registry_name` | `String` | Optional | The name of the container registry. |
| `tag_count` | `Integer` | Optional | The number of tags in the repository. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
repository = Repository.new(
  latest_tag: LatestTag.new(
    compressed_size_bytes: 108,
    manifest_digest: 'manifest_digest2',
    registry_name: 'registry_name4',
    repository: 'repository4',
    size_bytes: 226,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  name: 'repo-1',
  registry_name: 'example',
  tag_count: 1,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



