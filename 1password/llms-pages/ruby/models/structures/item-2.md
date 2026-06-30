# Item 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkl0ZW0y

*This model accepts additional fields of type Object.*


# Class Name

`Item2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
item2 = Item2.new(
  id: 'id2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



