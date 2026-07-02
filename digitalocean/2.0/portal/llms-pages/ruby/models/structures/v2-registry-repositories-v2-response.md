# V2 Registry Repositories V2 Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwUmVwb3NpdG9yaWVzVjIlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2RegistryRepositoriesV2Response`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `repositories` | [`Array[Repository1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/repository-1.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_registry_repositories_v2_response = V2RegistryRepositoriesV2Response.new(
  meta: Meta.new(
    total: 5,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  repositories: [
    Repository1.new(
      latest_manifest: LatestManifest.new(
        blobs: [
          Blob.new(
            compressed_size_bytes: 1471,
            digest: 'sha256:14119a10abf4669e8cdbdff324a9f9605d99697215a0d21c360fe8dfa8471bab',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          Blob.new(
            compressed_size_bytes: 12,
            digest: 'sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e',
            additional_properties: {
              'compressed_size_byte' => JSON.parse('2814446')
            }
          ),
          Blob.new(
            compressed_size_bytes: 528,
            digest: 'sha256:69704ef328d05a9f806b6b8502915e6a0a4faa4d72018dc42343f511490daf8a',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        compressed_size_bytes: 1972332,
        digest: 'sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221',
        registry_name: 'example',
        repository: 'repo-1',
        size_bytes: 2816445,
        tags: [
          'v1',
          'v2'
        ],
        updated_at: DateTimeHelper.from_rfc3339('2021-04-09T23:54:25Z'),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      manifest_count: 82,
      name: 'repo-1',
      registry_name: 'example',
      tag_count: 57,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  links: Links.new(
    pages: Pages.new(
      last: 'https://api.digitalocean.com/v2/registry/example/repositoriesV2?page=5&per_page=1',
      mnext: 'https://api.digitalocean.com/v2/registry/example/repositoriesV2?page=2&page_token=JPZmZzZXQiOjB9&per_page=1',
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



