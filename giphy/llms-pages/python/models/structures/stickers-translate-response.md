# Stickers Translate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/python/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBUcmFuc2xhdGUlMjUyMFJlc3BvbnNl


# Class Name

`StickersTranslateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/structures/gif.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |


# Example

```python
import dateutil.parser

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
        ]
    ),
    meta=Meta(
        msg='msg8',
        response_id='response_id0',
        status=98
    )
)
```



