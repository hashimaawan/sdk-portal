# V2 Databases Maintenance Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME1haW50ZW5hbmNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesMaintenanceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `day` | `String` | Required | The day of the week on which to apply maintenance updates. |
| `description` | `Array[String]` | Optional, Read-only | A list of strings, each containing information about a pending maintenance update. |
| `hour` | `String` | Required | The hour in UTC at which maintenance updates will be applied in 24 hour format. |
| `pending` | `TrueClass \| FalseClass` | Optional, Read-only | A boolean value indicating whether any maintenance is scheduled to be performed in the next window. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_maintenance_request = V2DatabasesMaintenanceRequest.new(
  day: 'tuesday',
  hour: '14:00',
  description: [
    'Update TimescaleDB to version 1.2.1',
    'Upgrade to PostgreSQL 11.2 and 10.7 bugfix releases'
  ],
  pending: true,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



