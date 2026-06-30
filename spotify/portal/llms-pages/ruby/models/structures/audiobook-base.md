# Audiobook Base

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkF1ZGlvYm9va0Jhc2U

*This model accepts additional fields of type Object.*


# Class Name

`AudiobookBase`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authors` | [`Array[AuthorObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/author-object.md) | Required | The author(s) for the audiobook. |
| `available_markets` | `Array[String]` | Required | A list of the countries in which the audiobook can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `copyrights` | [`Array[CopyrightObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/copyright-object.md) | Required | The copyright statements of the audiobook. |
| `description` | `String` | Required | A description of the audiobook. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `html_description` | `String` | Required | A description of the audiobook. This field may contain HTML tags. |
| `edition` | `String` | Optional | The edition of the audiobook. |
| `explicit` | `TrueClass \| FalseClass` | Required | Whether or not the audiobook has explicit content (true = yes it does; false = no it does not OR unknown). |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/external-url-object.md) | Required | External URLs for this audiobook. |
| `href` | `String` | Required | A link to the Web API endpoint providing full details of the audiobook. |
| `id` | `String` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `images` | [`Array[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/image-object.md) | Required | The cover art for the audiobook in various sizes, widest first. |
| `languages` | `Array[String]` | Required | A list of the languages used in the audiobook, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `media_type` | `String` | Required | The media type of the audiobook. |
| `name` | `String` | Required | The name of the audiobook. |
| `narrators` | [`Array[NarratorObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/narrator-object.md) | Required | The narrator(s) for the audiobook. |
| `publisher` | `String` | Required | The publisher of the audiobook. |
| `type` | `String` | Required, Constant | The object type.<br><br>**Value**: `'audiobook'` |
| `uri` | `String` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `total_chapters` | `Integer` | Required | The number of chapters in this audiobook. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
audiobook_base = AudiobookBase.new(
  authors: [
    AuthorObject.new(
      name: 'name0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  available_markets: [
    'available_markets2',
    'available_markets3'
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
  languages: [
    'languages5',
    'languages6'
  ],
  media_type: 'media_type4',
  name: 'name8',
  narrators: [
    NarratorObject.new(
      name: 'name0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  publisher: 'publisher4',
  type: 'audiobook',
  uri: 'uri2',
  total_chapters: 106,
  edition: 'Unabridged',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



