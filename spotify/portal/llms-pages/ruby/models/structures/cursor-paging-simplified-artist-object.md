# Cursor Paging Simplified Artist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ1NpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`CursorPagingSimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `limit` | `Integer` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Optional | URL to the next page of items. ( `null` if none) |
| `cursors` | [`CursorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `total` | `Integer` | Optional | The total number of items available to return. |
| `items` | [`Array[ArtistObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/artist-object.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
cursor_paging_simplified_artist_object = CursorPagingSimplifiedArtistObject.new(
  href: 'href8',
  limit: 172,
  mnext: 'next4',
  cursors: CursorObject.new(
    after: 'after8',
    before: 'before6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  total: 10,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



