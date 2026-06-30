# Paging Artist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlBhZ2luZ0FydGlzdE9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`PagingArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `Integer` | Required | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `Integer` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `String` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `Integer` | Required | The total number of items available to return. |
| `items` | [`Array[ArtistObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/artist-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
paging_artist_object = PagingArtistObject.new(
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  items: [
    ArtistObject.new(
      external_urls: ExternalUrlObject.new(
        spotify: 'spotify6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      followers: FollowersObject.new(
        href: 'href0',
        total: 82,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      genres: [
        'Prog rock',
        'Grunge'
      ],
      href: 'href0',
      id: 'id8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



