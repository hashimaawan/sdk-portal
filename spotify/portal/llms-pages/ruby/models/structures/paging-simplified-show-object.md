# Paging Simplified Show Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlBhZ2luZ1NpbXBsaWZpZWRTaG93T2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`PagingSimplifiedShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `Integer` | Required | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `Integer` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `String` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `Integer` | Required | The total number of items available to return. |
| `items` | [`Array[ShowBase]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/show-base.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
paging_simplified_show_object = PagingSimplifiedShowObject.new(
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  items: [
    ShowBase.new(
      available_markets: [
        'available_markets2'
      ],
      copyrights: [
        CopyrightObject.new(
          text: 'text2',
          type: 'type2',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      description: 'description2',
      html_description: 'html_description2',
      explicit: false,
      external_urls: ExternalUrlObject.new(
        spotify: 'spotify6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      href: 'href0',
      id: 'id8',
      images: [
        ImageObject.new(
          url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
          height: 300,
          width: 300,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      is_externally_hosted: false,
      languages: [
        'languages5'
      ],
      media_type: 'media_type4',
      name: 'name8',
      publisher: 'publisher4',
      type: 'show',
      uri: 'uri2',
      total_episodes: 166,
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



