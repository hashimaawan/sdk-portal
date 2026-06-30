# Episode Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkVwaXNvZGVPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`EpisodeObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `audio_preview_url` | `String` | Required | A URL to a 30 second preview (MP3 format) of the episode. `null` if not available. |
| `description` | `String` | Required | A description of the episode. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `html_description` | `String` | Required | A description of the episode. This field may contain HTML tags. |
| `duration_ms` | `Integer` | Required | The episode length in milliseconds. |
| `explicit` | `TrueClass \| FalseClass` | Required | Whether or not the episode has explicit content (true = yes it does; false = no it does not OR unknown). |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/external-url-object.md) | Required | External URLs for this episode. |
| `href` | `String` | Required | A link to the Web API endpoint providing full details of the episode. |
| `id` | `String` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the episode. |
| `images` | [`Array[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/image-object.md) | Required | The cover art for the episode in various sizes, widest first. |
| `is_externally_hosted` | `TrueClass \| FalseClass` | Required | True if the episode is hosted outside of Spotify's CDN. |
| `is_playable` | `TrueClass \| FalseClass` | Required | True if the episode is playable in the given market. Otherwise false. |
| `language` | `String` | Optional | The language used in the episode, identified by a [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. This field is deprecated and might be removed in the future. Please use the `languages` field instead. |
| `languages` | `Array[String]` | Required | A list of the languages used in the episode, identified by their [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639) code. |
| `name` | `String` | Required | The name of the episode. |
| `release_date` | `String` | Required | The date the episode was first released, for example `"1981-12-15"`. Depending on the precision, it might be shown as `"1981"` or `"1981-12"`. |
| `release_date_precision` | [`ReleaseDatePrecision`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `resume_point` | [`ResumePointObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/resume-point-object.md) | Optional | The user's most recent position in the episode. Set if the supplied access token is a user token and has the scope 'user-read-playback-position'. |
| `type` | `String` | Required, Constant | The object type.<br><br>**Value**: `'episode'` |
| `uri` | `String` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the episode. |
| `restrictions` | [`EpisodeRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/episode-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `show` | [`ShowBase`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/show-base.md) | Required | The show on which the episode belongs. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
episode_object = EpisodeObject.new(
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
  show: ShowBase.new(
    available_markets: [
      'available_markets0',
      'available_markets1',
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
    description: 'description4',
    html_description: 'html_description4',
    explicit: false,
    external_urls: ExternalUrlObject.new(
      spotify: 'spotify6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    href: 'href8',
    id: 'id6',
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
      'languages7',
      'languages6',
      'languages5'
    ],
    media_type: 'media_type6',
    name: 'name6',
    publisher: 'publisher6',
    type: 'show',
    uri: 'uri0',
    total_episodes: 198,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
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
```



