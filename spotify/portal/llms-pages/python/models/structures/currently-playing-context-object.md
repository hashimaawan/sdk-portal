# Currently Playing Context Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdDb250ZXh0T2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`CurrentlyPlayingContextObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `device` | [`DeviceObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/device-object.md) | Optional | The device that is currently active. |
| `repeat_state` | `str` | Optional | off, track, context |
| `shuffle_state` | `bool` | Optional | If shuffle is on or off. |
| `context` | [`ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `timestamp` | `int` | Optional | Unix Millisecond Timestamp when data was fetched. |
| `progress_ms` | `int` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `is_playing` | `bool` | Optional | If something is currently playing, return `true`. |
| `item` | [TrackObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/track-object.md) \| [EpisodeObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/episode-object.md) \| None | Optional | This is a container for one-of cases. |
| `currently_playing_type` | `str` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `actions` | [`DisallowsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.context_object import ContextObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.currently_playing_context_object import CurrentlyPlayingContextObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.device_object import DeviceObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject

currently_playing_context_object = CurrentlyPlayingContextObject(
    device=DeviceObject(
        id='id6',
        is_active=False,
        is_private_session=False,
        is_restricted=False,
        name='name6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    repeat_state='repeat_state8',
    shuffle_state=False,
    context=ContextObject(
        mtype='type8',
        href='href4',
        external_urls=ExternalUrlObject(
            spotify='spotify6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        uri='uri6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    timestamp=138,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



