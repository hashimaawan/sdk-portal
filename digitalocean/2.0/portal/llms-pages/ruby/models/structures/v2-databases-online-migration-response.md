# V2 Databases Online Migration Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesOnlineMigrationResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `String` | Optional | The time the migration was initiated, in ISO 8601 format. |
| `id` | `String` | Optional | The ID of the most recent migration. |
| `status` | [`Status5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status-5.md) | Optional | The current status of the migration. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_online_migration_response = V2DatabasesOnlineMigrationResponse.new(
  created_at: '2020-10-29T15:57:38Z',
  id: '77b28fc8-19ff-11eb-8c9c-c68e24557488',
  status: Status5::RUNNING,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



