# Cursor Paging Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ09iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`CursorPagingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `limit` | `Integer` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Optional | URL to the next page of items. ( `null` if none) |
| `cursors` | [`CursorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `total` | `Integer` | Optional | The total number of items available to return. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
cursor_paging_object = CursorPagingObject.new(
  href: 'href0',
  limit: 90,
  mnext: 'next4',
  cursors: CursorObject.new(
    after: 'after8',
    before: 'before6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  total: 184,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



