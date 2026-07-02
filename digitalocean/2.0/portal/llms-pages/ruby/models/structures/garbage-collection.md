# Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkdhcmJhZ2VDb2xsZWN0aW9u

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`GarbageCollection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blobs_deleted` | `Integer` | Optional | The number of blobs deleted as a result of this garbage collection. |
| `created_at` | `DateTime` | Optional | The time the garbage collection was created. |
| `freed_bytes` | `Integer` | Optional | The number of bytes freed as a result of this garbage collection. |
| `registry_name` | `String` | Optional | The name of the container registry. |
| `status` | [`Status15`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status-15.md) | Optional | The current status of this garbage collection. |
| `updated_at` | `DateTime` | Optional | The time the garbage collection was last updated. |
| `uuid` | `String` | Optional | A string specifying the UUID of the garbage collection. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
garbage_collection = GarbageCollection.new(
  blobs_deleted: 42,
  created_at: DateTimeHelper.from_rfc3339('2020-10-30T21:03:24Z'),
  freed_bytes: 667,
  registry_name: 'example',
  status: Status15::REQUESTED,
  updated_at: DateTimeHelper.from_rfc3339('2020-10-30T21:03:44Z'),
  uuid: 'eff0feee-49c7-4e8f-ba5c-a320c109c8a8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



