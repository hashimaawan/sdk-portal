# Paging Featured Playlist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlBhZ2luZ0ZlYXR1cmVkUGxheWxpc3RPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`PagingFeaturedPlaylistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `String` | Optional | The localized message of a playlist. |
| `playlists` | [`PagingPlaylistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/paging-playlist-object.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
paging_featured_playlist_object = PagingFeaturedPlaylistObject.new(
  message: 'Popular Playlists',
  playlists: PagingPlaylistObject.new(
    href: 'href2',
    limit: 68,
    mnext: 'next2',
    offset: 164,
    previous: 'previous8',
    total: 162,
    items: [
      SimplifiedPlaylistObject.new(
        collaborative: false,
        description: 'description2',
        external_urls: ExternalUrlObject.new(
          spotify: 'spotify6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        href: 'href0',
        id: 'id8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      SimplifiedPlaylistObject.new(
        collaborative: false,
        description: 'description2',
        external_urls: ExternalUrlObject.new(
          spotify: 'spotify6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        href: 'href0',
        id: 'id8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      SimplifiedPlaylistObject.new(
        collaborative: false,
        description: 'description2',
        external_urls: ExternalUrlObject.new(
          spotify: 'spotify6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
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
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



