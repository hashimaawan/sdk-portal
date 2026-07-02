# V2 Databases Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | [`Database1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/database-1.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_response1 = V2DatabasesResponse1.new(
  database: Database1.new(
    engine: Engine1::PG,
    name: 'backend',
    num_nodes: 2,
    region: 'nyc3',
    size: 'db-s-2vcpu-4gb',
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
    db_names: [
      'doadmin'
    ],
    id: '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
    maintenance_window: MaintenanceWindow.new(
      day: 'day0',
      hour: 'hour8',
      description: [
        'description3',
        'description2'
      ],
      pending: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    private_network_uuid: 'd455e75d-4858-4eec-8c95-da2f0a5f93a7',
    project_id: '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
    status: Status4::CREATING,
    tags: [
      'production'
    ],
    version: '10',
    version_end_of_availability: '2023-05-09T00:00:00Z',
    version_end_of_life: '2023-11-09T00:00:00Z',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



