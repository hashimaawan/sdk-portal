# Vault 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRlZhdWx0MQ

*This model accepts additional fields of type Object.*


# Class Name

`Vault1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
vault1 = Vault1.new(
  id: 'id0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



