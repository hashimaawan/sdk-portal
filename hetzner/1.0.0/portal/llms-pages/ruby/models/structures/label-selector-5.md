# Label Selector 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I1

Configuration for type label_selector, required if type is `label_selector`

*This model accepts additional fields of type Object.*


# Class Name

`LabelSelector5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `String` | Required | Label selector |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
label_selector5 = LabelSelector5.new(
  selector: 'env=prod',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



