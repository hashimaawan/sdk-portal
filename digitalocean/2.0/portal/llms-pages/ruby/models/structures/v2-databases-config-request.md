# V2 Databases Config Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesConfigRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `config` | [Config](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/config.md) \| [Config1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/config-1.md) \| [Config2](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/config-2.md) \| nil | Optional | This is a container for any-of cases. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_config_request = V2DatabasesConfigRequest.new(
  config: Config.new(
    backup_hour: 23,
    backup_minute: 59,
    binlog_retention_period: 600,
    connect_timeout: 196,
    default_time_zone: 'default_time_zone8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



