# Patch

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRlBhdGNo

*This model accepts additional fields of type Object.*


# Class Name

`Patch`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `op` | [`Op`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/op.md) | Required | - |
| `path` | `String` | Required | An RFC6901 JSON Pointer pointing to the Item document, an Item Attribute, and Item Field by Field ID, or an Item Field Attribute |
| `value` | `Object` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
patch = Patch.new(
  op: Op::REMOVE,
  path: '/fields/06gnn2b95example10q91512p5/label',
  value: { 'key1' => 'val1', 'key2' => 'val2' },
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



