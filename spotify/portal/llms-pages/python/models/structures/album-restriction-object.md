# Album Restriction Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRkFsYnVtUmVzdHJpY3Rpb25PYmplY3Q

*This model accepts additional fields of type Any.*


# Class Name

`AlbumRestrictionObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/enumerations/reason.md) | Optional | The reason for the restriction. Albums may be restricted if the content is not available in a given market, to the user's subscription type, or when the user's account is set to not play explicit content.<br>Additional reasons may be added in the future. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_restriction_object import AlbumRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.reason import Reason

album_restriction_object = AlbumRestrictionObject(
    reason=Reason.MARKET,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



