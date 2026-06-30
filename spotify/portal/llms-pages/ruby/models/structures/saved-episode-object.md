# Saved Episode Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlNhdmVkRXBpc29kZU9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`SavedEpisodeObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `added_at` | `DateTime` | Optional | The date and time the episode was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ. |
| `episode` | [`EpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/episode-object.md) | Optional | Information about the episode. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
saved_episode_object = SavedEpisodeObject.new(
  added_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  episode: EpisodeObject.new(
    audio_preview_url: 'audio_preview_url8',
    description: 'description2',
    html_description: 'html_description8',
    duration_ms: 46,
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
    is_externally_hosted: false,
    is_playable: false,
    languages: [
      'languages9',
      'languages0',
      'languages1'
    ],
    name: 'name2',
    release_date: 'release_date0',
    release_date_precision: ReleaseDatePrecision::YEAR,
    type: 'type8',
    uri: 'uri6',
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
      is_externally_hosted: false,
      languages: [
        'languages7',
        'languages6',
        'languages5'
      ],
      media_type: 'media_type6',
      name: 'name6',
      publisher: 'publisher6',
      type: 'type4',
      uri: 'uri0',
      total_episodes: 198,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    language: 'language4',
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
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



