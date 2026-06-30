# Me Player Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRk1lJTI1MjBQbGF5ZXIlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`MePlayerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `device_ids` | `List[str]` | Required | A JSON array containing the ID of the device on which playback should be started/transferred.<br/>For example:`{device_ids:["74ASZWbe4lXaubB36ztrGX"]}`<br/>_**Note**: Although an array is accepted, only a single device_id is currently supported. Supplying more than one will return `400 Bad Request`_ |
| `play` | `bool` | Optional | **true**: ensure playback happens on new device.<br/>**false** or not provided: keep the current playback state. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.me_player_request import MePlayerRequest

me_player_request = MePlayerRequest(
    device_ids=[
        '74ASZWbe4lXaubB36ztrGX'
    ],
    play=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



