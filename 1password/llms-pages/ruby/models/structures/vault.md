# Vault

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRlZhdWx0

*This model accepts additional fields of type Object.*


# Class Name

`Vault`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `attribute_version` | `Integer` | Optional | The vault version |
| `content_version` | `Integer` | Optional | The version of the vault contents |
| `created_at` | `DateTime` | Optional, Read-only | - |
| `description` | `String` | Optional | - |
| `id` | `String` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `items` | `Integer` | Optional | Number of active items in the vault |
| `name` | `String` | Optional | - |
| `type` | [`Type2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/type-2.md) | Optional | - |
| `updated_at` | `DateTime` | Optional, Read-only | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
vault = Vault.new(
  attribute_version: 108,
  content_version: 228,
  created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  description: 'description6',
  id: 'id6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



