# Action 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkFjdGlvbjQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Action4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_id` | `Integer` | Optional | A unique identifier for the resource that the action is associated with. |
| `type` | `String` | Optional | This is the type of action that the object represents. For example, this could be "attach_volume" to represent the state of a volume attach action. |
| `completed_at` | `DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. |
| `id` | `Integer` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/region.md) | Optional | - |
| `region_slug` | `String` | Optional | - |
| `resource_type` | `String` | Optional | The type of resource that the action is associated with. |
| `started_at` | `DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `Status1::INPROGRESS` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
action4 = Action4.new(
  resource_id: 160,
  type: 'attach_volume',
  completed_at: DateTimeHelper.from_rfc3339('2020-11-14T16:30:06Z'),
  id: 36804636,
  region: Region.new(
    available: false,
    features: [
      'features7',
      'features8',
      'features9'
    ],
    name: 'name6',
    sizes: [
      'sizes6'
    ],
    slug: 'slug0',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  resource_type: 'droplet',
  started_at: DateTimeHelper.from_rfc3339('2020-11-14T16:29:21Z'),
  status: Status1::COMPLETED,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



