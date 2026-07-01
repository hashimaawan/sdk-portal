# Label Selector 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I3

Label selector and a list of selected targets

*This model accepts additional fields of type Object.*


# Class Name

`LabelSelector7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `String` | Required | Label selector |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
label_selector7 = LabelSelector7.new(
  selector: 'env=prod',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



