# V2 Registry Garbage Collection Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwR2FyYmFnZSUyNTIwQ29sbGVjdGlvbiUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2RegistryGarbageCollectionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `garbage_collection` | [`GarbageCollection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/garbage-collection.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_registry_garbage_collection_response = V2RegistryGarbageCollectionResponse.new(
  garbage_collection: GarbageCollection.new(
    blobs_deleted: 40,
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    freed_bytes: 86,
    registry_name: 'registry_name6',
    status: Status15::SUCCEEDED,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



