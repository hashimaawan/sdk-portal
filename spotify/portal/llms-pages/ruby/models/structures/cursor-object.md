# Cursor Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkN1cnNvck9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`CursorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `after` | `String` | Optional | The cursor to use as key to find the next page of items. |
| `before` | `String` | Optional | The cursor to use as key to find the previous page of items. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
cursor_object = CursorObject.new(
  after: 'after8',
  before: 'before6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



