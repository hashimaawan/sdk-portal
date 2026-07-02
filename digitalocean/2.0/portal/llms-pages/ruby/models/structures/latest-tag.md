# Latest Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkxhdGVzdFRhZw

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`LatestTag`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `compressed_size_bytes` | `Integer` | Optional | The compressed size of the tag in bytes. |
| `manifest_digest` | `String` | Optional | The digest of the manifest associated with the tag. |
| `registry_name` | `String` | Optional | The name of the container registry. |
| `repository` | `String` | Optional | The name of the repository. |
| `size_bytes` | `Integer` | Optional | The uncompressed size of the tag in bytes (this size is calculated asynchronously so it may not be immediately available). |
| `tag` | `String` | Optional | The name of the tag. |
| `updated_at` | `DateTime` | Optional | The time the tag was last updated. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
latest_tag = LatestTag.new(
  compressed_size_bytes: 2803255,
  manifest_digest: 'sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221',
  registry_name: 'example',
  repository: 'repo-1',
  size_bytes: 5861888,
  tag: 'latest',
  updated_at: DateTimeHelper.from_rfc3339('2020-04-09T23:54:25Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



