# Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/python/x-redirect/JTI0bSUyRkdpZg


# Class Name

`Gif`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bitly_url` | `str` | Optional | The unique bit.ly URL for this GIF |
| `content_url` | `str` | Optional | Currently unused |
| `create_datetime` | `datetime` | Optional | The date this GIF was added to the GIPHY database. |
| `embded_url` | `str` | Optional | A URL used for embedding this GIF |
| `featured_tags` | `List[str]` | Optional | An array of featured tags for this GIF (Note: Not available when using the Public Beta Key) |
| `id` | `str` | Optional | This GIF's unique ID |
| `images` | [`Images`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/structures/images.md) | Optional | An object containing data for various available formats and sizes of this GIF. |
| `import_datetime` | `datetime` | Optional | The creation or upload date from this GIF's source. |
| `rating` | `str` | Optional | The MPAA-style rating for this content. Examples include Y, G, PG, PG-13 and R |
| `slug` | `str` | Optional | The unique slug used in this GIF's URL |
| `source` | `str` | Optional | The page on which this GIF was found |
| `source_post_url` | `str` | Optional | The URL of the webpage on which this GIF was found. |
| `source_tld` | `str` | Optional | The top level domain of the source URL. |
| `tags` | `List[str]` | Optional | An array of tags for this GIF (Note: Not available when using the Public Beta Key) |
| `trending_datetime` | `datetime` | Optional | The date on which this gif was marked trending, if applicable. |
| `mtype` | [`TypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/enumerations/type.md) | Optional | Type of the gif. By default, this is almost always gif<br><br>**Default**: `"gif"` |
| `update_datetime` | `datetime` | Optional | The date on which this GIF was last updated. |
| `url` | `str` | Optional | The unique URL for this GIF |
| `user` | [`User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/structures/user.md) | Optional | The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more. |
| `username` | `str` | Optional | The username this GIF is attached to, if applicable |


# Example

```python
import dateutil.parser

from giphyapi.models.gif import Gif
from giphyapi.models.type_enum import TypeEnum

gif = Gif(
    bitly_url='http://gph.is/1gsWDcL',
    content_url='content_url4',
    create_datetime=dateutil.parser.parse('2013-08-01 12:41:48'),
    embded_url='http://giphy.com/embed/YsTs5ltWtEhnq',
    featured_tags=[
        'featured_tags0'
    ],
    id='YsTs5ltWtEhnq',
    import_datetime=dateutil.parser.parse('2013-08-01 12:41:48'),
    rating='g',
    slug='confused-flying-YsTs5ltWtEhnq',
    source='http://www.reddit.com/r/reactiongifs/comments/1xpyaa/superman_goes_to_hollywood/',
    source_post_url='http://cheezburger.com/5282328320',
    source_tld='cheezburger.com',
    trending_datetime=dateutil.parser.parse('2013-08-01 12:41:48'),
    mtype=TypeEnum.GIF,
    update_datetime=dateutil.parser.parse('2013-08-01 12:41:48'),
    url='http://giphy.com/gifs/confused-flying-YsTs5ltWtEhnq',
    username='JoeCool4000'
)
```



