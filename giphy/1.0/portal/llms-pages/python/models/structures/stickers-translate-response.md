# Stickers Translate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/python/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBUcmFuc2xhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`StickersTranslateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/gif.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from giphyapi.models.gif import Gif
from giphyapi.models.meta import Meta
from giphyapi.models.stickers_translate_response import StickersTranslateResponse

stickers_translate_response = StickersTranslateResponse(
    data=Gif(
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
    meta=Meta(
        msg='msg8',
        response_id='response_id0',
        status=98,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



