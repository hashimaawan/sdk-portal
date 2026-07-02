# Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk5vZGU

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Node`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was created. |
| `droplet_id` | `String` | Optional | The ID of the Droplet used for the worker node. |
| `id` | `UUID \| String` | Optional | A unique ID that can be used to identify and reference the node. |
| `name` | `String` | Optional | An automatically generated, human-readable name for the node. |
| `status` | [`Status10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/status-10.md) | Optional | An object containing a `state` attribute whose value is set to a string indicating the current status of the node. |
| `updated_at` | `DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was last updated. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
node = Node.new(
  created_at: DateTimeHelper.from_rfc3339('2018-11-15T16:00:11Z'),
  droplet_id: '205545370',
  id: 'e78247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f',
  name: 'adoring-newton-3niq',
  status: Status10.new(
    state: State1::PROVISIONING,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  updated_at: DateTimeHelper.from_rfc3339('2018-11-15T16:00:11Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



