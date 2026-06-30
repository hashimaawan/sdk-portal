# Show Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRlNob3dPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`ShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available_markets` | `Array[String]` | Required | A list of the countries in which the show can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `copyrights` | [`Array[CopyrightObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/copyright-object.md) | Required | The copyright statements of the show. |
| `description` | `String` | Required | A description of the show. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `html_description` | `String` | Required | A description of the show. This field may contain HTML tags. |
| `explicit` | `TrueClass \| FalseClass` | Required | Whether or not the show has explicit content (true = yes it does; false = no it does not OR unknown). |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/external-url-object.md) | Required | External URLs for this show. |
| `href` | `String` | Required | A link to the Web API endpoint providing full details of the show. |
| `id` | `String` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `images` | [`Array[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/image-object.md) | Required | The cover art for the show in various sizes, widest first. |
| `is_externally_hosted` | `TrueClass \| FalseClass` | Required | True if all of the shows episodes are hosted outside of Spotify's CDN. This field might be `null` in some cases. |
| `languages` | `Array[String]` | Required | A list of the languages used in the show, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `media_type` | `String` | Required | The media type of the show. |
| `name` | `String` | Required | The name of the episode. |
| `publisher` | `String` | Required | The publisher of the show. |
| `type` | `String` | Required, Constant | The object type.<br><br>**Value**: `'show'` |
| `uri` | `String` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `total_episodes` | `Integer` | Required | The total number of episodes in the show. |
| `episodes` | [`PagingSimplifiedEpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/paging-simplified-episode-object.md) | Required | The episodes of the show. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
show_object = ShowObject.new(
  available_markets: [
    'available_markets6'
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
  description: 'description8',
  html_description: 'html_description8',
  explicit: false,
  external_urls: ExternalUrlObject.new(
    spotify: 'spotify6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  href: 'href4',
  id: 'id2',
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
    'languages1'
  ],
  media_type: 'media_type0',
  name: 'name2',
  publisher: 'publisher0',
  type: 'show',
  uri: 'uri6',
  total_episodes: 70,
  episodes: PagingSimplifiedEpisodeObject.new(
    href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
    limit: 20,
    mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    offset: 0,
    previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    total: 4,
    items: [
      EpisodeBase.new(
        audio_preview_url: 'https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17',
        description: 'A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.\n',
        html_description: '<p>A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.</p>\n',
        duration_ms: 1686230,
        explicit: false,
        external_urls: ExternalUrlObject.new(
          spotify: 'spotify6',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        href: 'https://api.spotify.com/v1/episodes/5Xt5DXGzch68nYYamXrNxZ',
        id: '5Xt5DXGzch68nYYamXrNxZ',
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
        is_playable: false,
        languages: [
          'fr',
          'en'
        ],
        name: 'Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators\n',
        release_date: '1981-12-15',
        release_date_precision: ReleaseDatePrecision::DAY,
        type: 'episode',
        uri: 'spotify:episode:0zLhl3WsOCQHbe1BPTiHgr',
        language: 'en',
        resume_point: ResumePointObject.new(
          fully_played: false,
          resume_position_ms: 254,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        restrictions: EpisodeRestrictionObject.new(
          reason: 'reason0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
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



