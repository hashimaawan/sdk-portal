# Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdpZg

*This model accepts additional fields of type Object.*


# Class Name

`Gif`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bitly_url` | `String` | Optional | The unique bit.ly URL for this GIF |
| `content_url` | `String` | Optional | Currently unused |
| `create_datetime` | `DateTime` | Optional | The date this GIF was added to the GIPHY database. |
| `embded_url` | `String` | Optional | A URL used for embedding this GIF |
| `featured_tags` | `Array[String]` | Optional | An array of featured tags for this GIF (Note: Not available when using the Public Beta Key) |
| `id` | `String` | Optional | This GIF's unique ID |
| `images` | [`Images`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/images.md) | Optional | An object containing data for various available formats and sizes of this GIF. |
| `import_datetime` | `DateTime` | Optional | The creation or upload date from this GIF's source. |
| `rating` | `String` | Optional | The MPAA-style rating for this content. Examples include Y, G, PG, PG-13 and R |
| `slug` | `String` | Optional | The unique slug used in this GIF's URL |
| `source` | `String` | Optional | The page on which this GIF was found |
| `source_post_url` | `String` | Optional | The URL of the webpage on which this GIF was found. |
| `source_tld` | `String` | Optional | The top level domain of the source URL. |
| `tags` | `Array[String]` | Optional | An array of tags for this GIF (Note: Not available when using the Public Beta Key) |
| `trending_datetime` | `DateTime` | Optional | The date on which this gif was marked trending, if applicable. |
| `type` | [`Type`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/enumerations/type.md) | Optional | Type of the gif. By default, this is almost always gif<br><br>**Default**: `Type::GIF` |
| `update_datetime` | `DateTime` | Optional | The date on which this GIF was last updated. |
| `url` | `String` | Optional | The unique URL for this GIF |
| `user` | [`User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/user.md) | Optional | The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more. |
| `username` | `String` | Optional | The username this GIF is attached to, if applicable |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
gif = Gif.new(
  bitly_url: 'http://gph.is/1gsWDcL',
  content_url: 'content_url4',
  create_datetime: DateTimeHelper.from_rfc3339('2013-08-01 12:41:48'),
  embded_url: 'http://giphy.com/embed/YsTs5ltWtEhnq',
  featured_tags: [
    'featured_tags0'
  ],
  id: 'YsTs5ltWtEhnq',
  import_datetime: DateTimeHelper.from_rfc3339('2013-08-01 12:41:48'),
  rating: 'g',
  slug: 'confused-flying-YsTs5ltWtEhnq',
  source: 'http://www.reddit.com/r/reactiongifs/comments/1xpyaa/superman_goes_to_hollywood/',
  source_post_url: 'http://cheezburger.com/5282328320',
  source_tld: 'cheezburger.com',
  trending_datetime: DateTimeHelper.from_rfc3339('2013-08-01 12:41:48'),
  type: Type::GIF,
  update_datetime: DateTimeHelper.from_rfc3339('2013-08-01 12:41:48'),
  url: 'http://giphy.com/gifs/confused-flying-YsTs5ltWtEhnq',
  username: 'JoeCool4000',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



