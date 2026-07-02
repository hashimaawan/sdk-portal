# V2 Databases Replicas Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlcGxpY2FzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesReplicasResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `replica` | [`Replica`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/replica.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_replicas_response1 = V2DatabasesReplicasResponse1.new(
  replica: Replica.new(
    name: 'name6',
    connection: Connection.new(
      database: 'database2',
      host: 'host0',
      password: 'password2',
      port: 174,
      ssl: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    id: '000007e0-0000-0000-0000-000000000000',
    private_connection: PrivateConnection.new(
      database: 'database4',
      host: 'host4',
      password: 'password8',
      port: 228,
      ssl: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    private_network_uuid: 'private_network_uuid6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



