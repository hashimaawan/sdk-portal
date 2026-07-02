# V2 Databases Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databases` | [`Array[Database1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/database-1.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_response = V2DatabasesResponse.new(
  databases: [
    Database1.new(
      engine: Engine1::REDIS,
      name: 'name6',
      num_nodes: 242,
      region: 'region2',
      size: 'size4',
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
      db_names: [
        'db_names7',
        'db_names8'
      ],
      id: '0000031c-0000-0000-0000-000000000000',
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
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Database1.new(
      engine: Engine1::REDIS,
      name: 'name6',
      num_nodes: 242,
      region: 'region2',
      size: 'size4',
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
      db_names: [
        'db_names7',
        'db_names8'
      ],
      id: '0000031c-0000-0000-0000-000000000000',
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
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Database1.new(
      engine: Engine1::REDIS,
      name: 'name6',
      num_nodes: 242,
      region: 'region2',
      size: 'size4',
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
      db_names: [
        'db_names7',
        'db_names8'
      ],
      id: '0000031c-0000-0000-0000-000000000000',
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



