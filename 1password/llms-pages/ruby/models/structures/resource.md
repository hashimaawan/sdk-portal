# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRlJlc291cmNl

*This model accepts additional fields of type Object.*


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `item` | [`Item2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/item-2.md) | Optional | - |
| `item_version` | `Integer` | Optional | - |
| `type` | [`Type`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/type.md) | Optional | - |
| `vault` | [`Vault3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/vault-3.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
resource = Resource.new(
  item: Item2.new(
    id: 'id2',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  item_version: 108,
  type: Type::ITEM,
  vault: Vault3.new(
    id: 'id6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



