# Gifs Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/python/x-redirect/JTI0bSUyRkdpZnMlMjUyMFJlc3BvbnNl


# Class Name

`GifsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`List[Gif]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/structures/gif.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |
| `pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. |


# Example

```python
import dateutil.parser

from giphyapi.models.gif import Gif
from giphyapi.models.gifs_response import GifsResponse
from giphyapi.models.meta import Meta
from giphyapi.models.pagination import Pagination

gifs_response = GifsResponse(
    data=[
        Gif(
            bitly_url='bitly_url0',
            content_url='content_url4',
            create_datetime=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            embded_url='embded_url8',
            featured_tags=[
                'featured_tags0'
            ]
        )
    ],
    meta=Meta(
        msg='msg8',
        response_id='response_id0',
        status=98
    ),
    pagination=Pagination(
        count=192,
        offset=240,
        total_count=100
    )
)
```



