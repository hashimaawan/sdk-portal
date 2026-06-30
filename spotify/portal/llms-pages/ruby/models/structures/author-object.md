# Author Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkF1dGhvck9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`AuthorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | The name of the author. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
author_object = AuthorObject.new(
  name: 'name8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



