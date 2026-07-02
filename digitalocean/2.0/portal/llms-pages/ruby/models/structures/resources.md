# Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc291cmNlcw

An object containing additional information about resource related to a Droplet requested to be destroyed.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Resources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floating_ips` | [`Array[Droplet1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/droplet-1.md) | Optional | - |
| `reserved_ips` | [`Array[Droplet1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/droplet-1.md) | Optional | - |
| `snapshots` | [`Array[Droplet1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/droplet-1.md) | Optional | - |
| `volume_snapshots` | [`Array[Droplet1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/droplet-1.md) | Optional | - |
| `volumes` | [`Array[Droplet1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/droplet-1.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
resources = Resources.new(
  floating_ips: [
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message4',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message4',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message4',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  reserved_ips: [
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message2',
      id: 'id0',
      name: 'name0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message2',
      id: 'id0',
      name: 'name0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  snapshots: [
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message4',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message4',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message4',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  volume_snapshots: [
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message0',
      id: 'id8',
      name: 'name8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message0',
      id: 'id8',
      name: 'name8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  volumes: [
    Droplet1.new(
      destroyed_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      error_message: 'error_message8',
      id: 'id6',
      name: 'name6',
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



