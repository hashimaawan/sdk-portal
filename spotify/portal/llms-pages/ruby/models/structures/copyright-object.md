# Copyright Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRkNvcHlyaWdodE9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`CopyrightObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `text` | `String` | Optional | The copyright text for this content. |
| `type` | `String` | Optional | The type of copyright: `C` = the copyright, `P` = the sound recording (performance) copyright. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
copyright_object = CopyrightObject.new(
  text: 'text6',
  type: 'type6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



