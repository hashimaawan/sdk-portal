# Vault 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRlZhdWx0Mw

*This model accepts additional fields of type Object.*


# Class Name

`Vault3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
vault3 = Vault3.new(
  id: 'id0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



