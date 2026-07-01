# Label Selector 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3Ix

Configuration for type LabelSelector, required if type is `label_selector`

*This model accepts additional fields of type Object.*


# Class Name

`LabelSelector1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `String` | Required | Label selector |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
label_selector1 = LabelSelector1.new(
  selector: 'selector2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



