# Many Episodes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRk1hbnlFcGlzb2Rlcw

*This model accepts additional fields of type Object.*


# Class Name

`ManyEpisodes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `episodes` | [`Array[EpisodeObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/episode-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
many_episodes = ManyEpisodes.new(
  episodes: [
    EpisodeObject.new(
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
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



