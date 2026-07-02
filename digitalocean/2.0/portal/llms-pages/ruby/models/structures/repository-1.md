# Repository 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlcG9zaXRvcnkx

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Repository1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `latest_manifest` | [`LatestManifest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/latest-manifest.md) | Optional | - |
| `manifest_count` | `Integer` | Optional | The number of manifests in the repository. |
| `name` | `String` | Optional | The name of the repository. |
| `registry_name` | `String` | Optional | The name of the container registry. |
| `tag_count` | `Integer` | Optional | The number of tags in the repository. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
repository1 = Repository1.new(
  latest_manifest: LatestManifest.new(
    blobs: [
      Blob.new(
        compressed_size_bytes: 12,
        digest: 'digest2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Blob.new(
        compressed_size_bytes: 12,
        digest: 'digest2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Blob.new(
        compressed_size_bytes: 12,
        digest: 'digest2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    compressed_size_bytes: 154,
    digest: 'digest0',
    registry_name: 'registry_name4',
    repository: 'repository4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  manifest_count: 1,
  name: 'repo-1',
  registry_name: 'example',
  tag_count: 1,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



