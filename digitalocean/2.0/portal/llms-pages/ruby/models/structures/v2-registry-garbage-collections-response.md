# V2 Registry Garbage Collections Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwR2FyYmFnZSUyNTIwQ29sbGVjdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2RegistryGarbageCollectionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `garbage_collections` | [`Array[GarbageCollection]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/garbage-collection.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_registry_garbage_collections_response = V2RegistryGarbageCollectionsResponse.new(
  garbage_collections: [
    GarbageCollection.new(
      blobs_deleted: 26,
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      freed_bytes: 100,
      registry_name: 'registry_name2',
      status: Status15::REQUESTED,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    GarbageCollection.new(
      blobs_deleted: 26,
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      freed_bytes: 100,
      registry_name: 'registry_name2',
      status: Status15::REQUESTED,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    GarbageCollection.new(
      blobs_deleted: 26,
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      freed_bytes: 100,
      registry_name: 'registry_name2',
      status: Status15::REQUESTED,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



