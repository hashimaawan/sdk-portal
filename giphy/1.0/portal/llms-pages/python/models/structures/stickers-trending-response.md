# Stickers Trending Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/python/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBUcmVuZGluZyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Any.*


# Class Name

`StickersTrendingResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`List[Gif]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/gif.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |
| `pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from giphyapi.models.gif import Gif
from giphyapi.models.meta import Meta
from giphyapi.models.pagination import Pagination
from giphyapi.models.stickers_trending_response import StickersTrendingResponse

stickers_trending_response = StickersTrendingResponse(
    data=[
        Gif(
            bitly_url='bitly_url0',
            content_url='content_url4',
            create_datetime=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            embded_url='embded_url8',
            featured_tags=[
                'featured_tags0'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Gif(
            bitly_url='bitly_url0',
            content_url='content_url4',
            create_datetime=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            embded_url='embded_url8',
            featured_tags=[
                'featured_tags0'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    meta=Meta(
        msg='msg8',
        response_id='response_id0',
        status=98,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    pagination=Pagination(
        count=192,
        offset=240,
        total_count=100,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



