# Cursor Paged Artists

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkN1cnNvclBhZ2VkQXJ0aXN0cw

*This model accepts additional fields of type Object.*


# Class Name

`CursorPagedArtists`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `artists` | [`CursorPagingSimplifiedArtistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/cursor-paging-simplified-artist-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
cursor_paged_artists = CursorPagedArtists.new(
  artists: CursorPagingSimplifiedArtistObject.new(
    href: 'href2',
    limit: 214,
    mnext: 'next2',
    cursors: CursorObject.new(
      after: 'after8',
      before: 'before6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    total: 52,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



