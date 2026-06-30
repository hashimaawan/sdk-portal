# Cursor Paging Play History Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ1BsYXlIaXN0b3J5T2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`CursorPagingPlayHistoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `limit` | `Integer` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Optional | URL to the next page of items. ( `null` if none) |
| `cursors` | [`CursorObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `total` | `Integer` | Optional | The total number of items available to return. |
| `items` | [`Array[PlayHistoryObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/play-history-object.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
cursor_paging_play_history_object = CursorPagingPlayHistoryObject.new(
  href: 'href0',
  limit: 234,
  mnext: 'next6',
  cursors: CursorObject.new(
    after: 'after8',
    before: 'before6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  total: 72,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



