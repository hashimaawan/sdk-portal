# V2 Databases Upgrade Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVwZ3JhZGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DatabasesUpgradeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `version` | `String` | Optional | A string representing the version of the database engine in use for the cluster. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_databases_upgrade_request = V2DatabasesUpgradeRequest.new(
  version: '10',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



