# Replica

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlcGxpY2E

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Replica`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `connection` | [`Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/connection.md) | Optional | - |
| `created_at` | `DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. |
| `id` | `UUID \| String` | Optional, Read-only | A unique ID that can be used to identify and reference a database replica. |
| `name` | `String` | Required | The name to give the read-only replicating |
| `private_connection` | [`PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/private-connection.md) | Optional | - |
| `private_network_uuid` | `String` | Optional | A string specifying the UUID of the VPC to which the read-only replica will be assigned. If excluded, the replica will be assigned to your account's default VPC for the region. |
| `region` | `String` | Optional | A slug identifier for the region where the read-only replica will be located. If excluded, the replica will be placed in the same region as the cluster. |
| `size` | `String` | Optional | A slug identifier representing the size of the node for the read-only replica. The size of the replica must be at least as large as the node size for the database cluster from which it is replicating. |
| `status` | [`Status4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. |
| `tags` | `Array[String]` | Optional | A flat array of tag names as strings to apply to the read-only replica after it is created. Tag names can either be existing or new tags. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
replica = Replica.new(
  name: 'read-nyc3-01',
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
  created_at: DateTimeHelper.from_rfc3339('2019-01-11T18:37:36Z'),
  id: '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
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
  private_network_uuid: '9423cbad-9211-442f-820b-ef6915e99b5f',
  region: 'nyc3',
  size: 'db-s-2vcpu-4gb',
  status: Status4::CREATING,
  tags: [
    'production'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



