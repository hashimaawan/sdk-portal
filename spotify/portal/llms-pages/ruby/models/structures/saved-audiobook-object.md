# Saved Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRlNhdmVkQXVkaW9ib29rT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`SavedAudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `added_at` | `DateTime` | Optional | The date and time the audiobook was saved<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `audiobook` | [`AudiobookObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/audiobook-object.md) | Optional | Information about the audiobook. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
saved_audiobook_object = SavedAudiobookObject.new(
  added_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  audiobook: AudiobookObject.new(
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
      ),
      CopyrightObject.new(
        text: 'text2',
        type: 'type2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
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
        url: 'url6',
        height: 182,
        width: 222,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      ImageObject.new(
        url: 'url6',
        height: 182,
        width: 222,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      ImageObject.new(
        url: 'url6',
        height: 182,
        width: 222,
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
      ),
      NarratorObject.new(
        name: 'name0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    publisher: 'publisher4',
    type: 'type2',
    uri: 'uri2',
    total_chapters: 186,
    chapters: PagingSimplifiedChapterObject.new(
      href: 'href4',
      limit: 230,
      mnext: 'next0',
      offset: 122,
      previous: 'previous0',
      total: 136,
      items: [
        ChapterBase.new(
          audio_preview_url: 'audio_preview_url4',
          chapter_number: 164,
          description: 'description2',
          html_description: 'html_description2',
          duration_ms: 52,
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
              url: 'url6',
              height: 182,
              width: 222,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            ImageObject.new(
              url: 'url6',
              height: 182,
              width: 222,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            )
          ],
          is_playable: false,
          languages: [
            'languages5'
          ],
          name: 'name8',
          release_date: 'release_date6',
          release_date_precision: ReleaseDatePrecision::MONTH,
          type: 'type2',
          uri: 'uri2',
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
    edition: 'edition8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



