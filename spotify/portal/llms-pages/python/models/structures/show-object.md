# Show Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlNob3dPYmplY3Q

*This model accepts additional fields of type Any.*


# Class Name

`ShowObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available_markets` | `List[str]` | Required | A list of the countries in which the show can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `copyrights` | [`List[CopyrightObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/copyright-object.md) | Required | The copyright statements of the show. |
| `description` | `str` | Required | A description of the show. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `html_description` | `str` | Required | A description of the show. This field may contain HTML tags. |
| `explicit` | `bool` | Required | Whether or not the show has explicit content (true = yes it does; false = no it does not OR unknown). |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/external-url-object.md) | Required | External URLs for this show. |
| `href` | `str` | Required | A link to the Web API endpoint providing full details of the show. |
| `id` | `str` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `images` | [`List[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/image-object.md) | Required | The cover art for the show in various sizes, widest first. |
| `is_externally_hosted` | `bool` | Required | True if all of the shows episodes are hosted outside of Spotify's CDN. This field might be `null` in some cases. |
| `languages` | `List[str]` | Required | A list of the languages used in the show, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `media_type` | `str` | Required | The media type of the show. |
| `name` | `str` | Required | The name of the episode. |
| `publisher` | `str` | Required | The publisher of the show. |
| `mtype` | `str` | Required, Constant | The object type.<br><br>**Value**: `"show"` |
| `uri` | `str` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `total_episodes` | `int` | Required | The total number of episodes in the show. |
| `episodes` | [`PagingSimplifiedEpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/paging-simplified-episode-object.md) | Required | The episodes of the show. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.episode_base import EpisodeBase
from spotifywebapiwithfixesandimprovementsfromsonallux.models.episode_restriction_object import EpisodeRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_simplified_episode_object import PagingSimplifiedEpisodeObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.resume_point_object import ResumePointObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.show_object import ShowObject

show_object = ShowObject(
    available_markets=[
        'available_markets6'
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
    description='description8',
    html_description='html_description8',
    explicit=False,
    external_urls=ExternalUrlObject(
        spotify='spotify6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    href='href4',
    id='id2',
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
        'languages1'
    ],
    media_type='media_type0',
    name='name2',
    publisher='publisher0',
    uri='uri6',
    total_episodes=70,
    episodes=PagingSimplifiedEpisodeObject(
        href='https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
        limit=20,
        next='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
        offset=0,
        previous='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
        total=4,
        items=[
            EpisodeBase(
                audio_preview_url='https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17',
                description='A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.\n',
                html_description='<p>A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.</p>\n',
                duration_ms=1686230,
                explicit=False,
                external_urls=ExternalUrlObject(
                    spotify='spotify6',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                href='https://api.spotify.com/v1/episodes/5Xt5DXGzch68nYYamXrNxZ',
                id='5Xt5DXGzch68nYYamXrNxZ',
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
                is_playable=False,
                languages=[
                    'fr',
                    'en'
                ],
                name='Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators\n',
                release_date='1981-12-15',
                release_date_precision=ReleaseDatePrecision.DAY,
                uri='spotify:episode:0zLhl3WsOCQHbe1BPTiHgr',
                language='en',
                resume_point=ResumePointObject(
                    fully_played=False,
                    resume_position_ms=254,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                restrictions=EpisodeRestrictionObject(
                    reason='reason0',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



