# Simplified Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRBbGJ1bU9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`SimplifiedAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `album_type` | [`AlbumType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/enumerations/album-type.md) | Required | The type of the album. |
| `total_tracks` | `Integer` | Required | The number of tracks in the album. |
| `available_markets` | `Array[String]` | Required | The markets in which the album is available: [ISO 3166-1 alpha-2 country codes](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _**NOTE**: an album is considered available in a market when at least 1 of its tracks is available in that market._ |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/external-url-object.md) | Required | Known external URLs for this album. |
| `href` | `String` | Required | A link to the Web API endpoint providing full details of the album. |
| `id` | `String` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `images` | [`Array[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/image-object.md) | Required | The cover art for the album in various sizes, widest first. |
| `name` | `String` | Required | The name of the album. In case of an album takedown, the value may be an empty string. |
| `release_date` | `String` | Required | The date the album was first released. |
| `release_date_precision` | [`ReleaseDatePrecision`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `restrictions` | [`AlbumRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/album-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `type` | `String` | Required, Constant | The object type.<br><br>**Value**: `'album'` |
| `uri` | `String` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `artists` | [`Array[SimplifiedArtistObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/simplified-artist-object.md) | Required | The artists of the album. Each artist object includes a link in `href` to more detailed information about the artist. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
simplified_album_object = SimplifiedAlbumObject.new(
  album_type: AlbumType::COMPILATION,
  total_tracks: 9,
  available_markets: [
    'CA',
    'BR',
    'IT'
  ],
  external_urls: ExternalUrlObject.new(
    spotify: 'spotify6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  href: 'href4',
  id: '2up3OPMp9Tb4dAKM2erWXQ',
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
  name: 'name2',
  release_date: '1981-12',
  release_date_precision: ReleaseDatePrecision::YEAR,
  type: 'album',
  uri: 'spotify:album:2up3OPMp9Tb4dAKM2erWXQ',
  artists: [
    SimplifiedArtistObject.new(
      external_urls: ExternalUrlObject.new(
        spotify: 'spotify6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      href: 'href2',
      id: 'id0',
      name: 'name0',
      type: Type::ARTIST,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  restrictions: AlbumRestrictionObject.new(
    reason: Reason::EXPLICIT,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



