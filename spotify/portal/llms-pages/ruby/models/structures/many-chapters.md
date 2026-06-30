# Many Chapters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRk1hbnlDaGFwdGVycw

*This model accepts additional fields of type Object.*


# Class Name

`ManyChapters`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `chapters` | [`Array[ChapterObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/chapter-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
many_chapters = ManyChapters.new(
  chapters: [
    ChapterObject.new(
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
      audiobook: AudiobookBase.new(
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
          'available_markets3',
          'available_markets4'
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
        languages: [
          'languages3',
          'languages4'
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
        total_chapters: 186,
        edition: 'Unabridged',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      available_markets: [
        'available_markets6',
        'available_markets7'
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
)
```



