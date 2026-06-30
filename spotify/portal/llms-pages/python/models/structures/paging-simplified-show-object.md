# Paging Simplified Show Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlBhZ2luZ1NpbXBsaWZpZWRTaG93T2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`PagingSimplifiedShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `next` | `str` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `str` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `int` | Required | The total number of items available to return. |
| `items` | [`List[ShowBase]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/show-base.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_simplified_show_object import PagingSimplifiedShowObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.show_base import ShowBase

paging_simplified_show_object = PagingSimplifiedShowObject(
    href='https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
    limit=20,
    next='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    offset=0,
    previous='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    total=4,
    items=[
        ShowBase(
            available_markets=[
                'available_markets2'
            ],
            copyrights=[
                CopyrightObject(
                    text='text2',
                    mtype='type2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            description='description2',
            html_description='html_description2',
            explicit=False,
            external_urls=ExternalUrlObject(
                spotify='spotify6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            href='href0',
            id='id8',
            images=[
                ImageObject(
                    url='https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
                    height=300,
                    width=300,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            is_externally_hosted=False,
            languages=[
                'languages5'
            ],
            media_type='media_type4',
            name='name8',
            publisher='publisher4',
            uri='uri2',
            total_episodes=166,
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



