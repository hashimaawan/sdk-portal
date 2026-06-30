# Currently Playing Context Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdDb250ZXh0T2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`CurrentlyPlayingContextObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `device` | [`DeviceObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/device-object.md) | Optional | The device that is currently active. |
| `repeat_state` | `String` | Optional | off, track, context |
| `shuffle_state` | `TrueClass \| FalseClass` | Optional | If shuffle is on or off. |
| `context` | [`ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `timestamp` | `Integer` | Optional | Unix Millisecond Timestamp when data was fetched. |
| `progress_ms` | `Integer` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `is_playing` | `TrueClass \| FalseClass` | Optional | If something is currently playing, return `true`. |
| `item` | [TrackObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/track-object.md) \| [EpisodeObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/episode-object.md) \| nil | Optional | This is a container for one-of cases. |
| `currently_playing_type` | `String` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `actions` | [`DisallowsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/ruby/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
currently_playing_context_object = CurrentlyPlayingContextObject.new(
  device: DeviceObject.new(
    id: 'id6',
    is_active: false,
    is_private_session: false,
    is_restricted: false,
    name: 'name6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  repeat_state: 'repeat_state8',
  shuffle_state: false,
  context: ContextObject.new(
    type: 'type8',
    href: 'href4',
    external_urls: ExternalUrlObject.new(
      spotify: 'spotify6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    uri: 'uri6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  timestamp: 138,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



