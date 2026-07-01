# Labels 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxhYmVsczI

User-defined labels (key-value pairs)

*This model accepts additional fields of type Object.*


# Class Name

`Labels2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelkey` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
labels2 = Labels2.new(
  labelkey: 'value',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



