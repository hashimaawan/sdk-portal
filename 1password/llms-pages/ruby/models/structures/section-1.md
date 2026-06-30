# Section 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRlNlY3Rpb24x

For files that are in a section, this field describes the section.

*This model accepts additional fields of type Object.*


# Class Name

`Section1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
section1 = Section1.new(
  id: 'id2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



