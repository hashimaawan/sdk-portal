# Paging Saved Audiobook Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRlBhZ2luZ1NhdmVkQXVkaW9ib29rT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`PagingSavedAudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `Integer` | Required | The maximum number of items in the response (as set in the query or by default). |
| `mnext` | `String` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `Integer` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `String` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `Integer` | Required | The total number of items available to return. |
| `items` | [`Array[SavedAudiobookObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/saved-audiobook-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
paging_saved_audiobook_object = PagingSavedAudiobookObject.new(
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  mnext: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  items: [
    SavedAudiobookObject.new(
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
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



