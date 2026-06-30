# Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkF1ZGlvYm9va09iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`AudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authors` | [`Array[AuthorObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/author-object.md) | Required | The author(s) for the audiobook. |
| `available_markets` | `Array[String]` | Required | A list of the countries in which the audiobook can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `copyrights` | [`Array[CopyrightObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/copyright-object.md) | Required | The copyright statements of the audiobook. |
| `description` | `String` | Required | A description of the audiobook. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `html_description` | `String` | Required | A description of the audiobook. This field may contain HTML tags. |
| `edition` | `String` | Optional | The edition of the audiobook. |
| `explicit` | `TrueClass \| FalseClass` | Required | Whether or not the audiobook has explicit content (true = yes it does; false = no it does not OR unknown). |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/external-url-object.md) | Required | External URLs for this audiobook. |
| `href` | `String` | Required | A link to the Web API endpoint providing full details of the audiobook. |
| `id` | `String` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `images` | [`Array[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/image-object.md) | Required | The cover art for the audiobook in various sizes, widest first. |
| `languages` | `Array[String]` | Required | A list of the languages used in the audiobook, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `media_type` | `String` | Required | The media type of the audiobook. |
| `name` | `String` | Required | The name of the audiobook. |
| `narrators` | [`Array[NarratorObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/narrator-object.md) | Required | The narrator(s) for the audiobook. |
| `publisher` | `String` | Required | The publisher of the audiobook. |
| `type` | `String` | Required, Constant | The object type.<br><br>**Value**: `'audiobook'` |
| `uri` | `String` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `total_chapters` | `Integer` | Required | The number of chapters in this audiobook. |
| `chapters` | [`PagingSimplifiedChapterObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/paging-simplified-chapter-object.md) | Required | The chapters of the audiobook. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
audiobook_object = AudiobookObject.new(
  authors: [
    AuthorObject.new(
      name: 'name0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  available_markets: [
    'available_markets8',
    'available_markets9',
    'available_markets0'
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
  href: 'href6',
  id: 'id4',
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
  languages: [
    'languages1',
    'languages2',
    'languages3'
  ],
  media_type: 'media_type2',
  name: 'name4',
  narrators: [
    NarratorObject.new(
      name: 'name0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  publisher: 'publisher2',
  type: 'audiobook',
  uri: 'uri8',
  total_chapters: 196,
  chapters: PagingSimplifiedChapterObject.new(
    href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
    limit: 20,
    mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    offset: 0,
    previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    total: 4,
    items: [
      ChapterBase.new(
        audio_preview_url: 'https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17',
        chapter_number: 1,
        description: 'We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.\n',
        html_description: '<p>We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.</p>\n',
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
        available_markets: [
          'available_markets2'
        ],
        resume_point: ResumePointObject.new(
          fully_played: false,
          resume_position_ms: 254,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        restrictions: ChapterRestrictionObject.new(
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
  edition: 'Unabridged',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



