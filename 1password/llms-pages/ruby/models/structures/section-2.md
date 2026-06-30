# Section 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRlNlY3Rpb24y

*This model accepts additional fields of type Object.*


# Class Name

`Section2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | - |
| `label` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
section2 = Section2.new(
  id: 'id4',
  label: 'label4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



