# Many Artists

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRk1hbnlBcnRpc3Rz

*This model accepts additional fields of type Any.*


# Class Name

`ManyArtists`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `artists` | [`List[ArtistObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/artist-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.artist_object import ArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.followers_object import FollowersObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.many_artists import ManyArtists

many_artists = ManyArtists(
    artists=[
        ArtistObject(
            external_urls=ExternalUrlObject(
                spotify='spotify6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            followers=FollowersObject(
                href='href0',
                total=82,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            genres=[
                'Prog rock',
                'Grunge'
            ],
            href='href2',
            id='id0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



