# Many Audiobooks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRk1hbnlBdWRpb2Jvb2tz

*This model accepts additional fields of type Any.*


# Class Name

`ManyAudiobooks`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `audiobooks` | [`List[AudiobookObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/audiobook-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.audiobook_object import AudiobookObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.author_object import AuthorObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.chapter_base import ChapterBase
from spotifywebapiwithfixesandimprovementsfromsonallux.models.chapter_restriction_object import ChapterRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.many_audiobooks import ManyAudiobooks
from spotifywebapiwithfixesandimprovementsfromsonallux.models.narrator_object import NarratorObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_simplified_chapter_object import PagingSimplifiedChapterObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.resume_point_object import ResumePointObject

many_audiobooks = ManyAudiobooks(
    audiobooks=[
        AudiobookObject(
            authors=[
                AuthorObject(
                    name='name0',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            available_markets=[
                'available_markets8'
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
            description='description4',
            html_description='html_description6',
            explicit=False,
            external_urls=ExternalUrlObject(
                spotify='spotify6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            href='href6',
            id='id4',
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
            languages=[
                'languages1'
            ],
            media_type='media_type8',
            name='name4',
            narrators=[
                NarratorObject(
                    name='name0',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            publisher='publisher8',
            uri='uri8',
            total_chapters=186,
            chapters=PagingSimplifiedChapterObject(
                href='https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
                limit=20,
                next='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
                offset=0,
                previous='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
                total=4,
                items=[
                    ChapterBase(
                        audio_preview_url='https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17',
                        chapter_number=1,
                        description='We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.\n',
                        html_description='<p>We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.</p>\n',
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
                        is_playable=False,
                        languages=[
                            'fr',
                            'en'
                        ],
                        name='Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators\n',
                        release_date='1981-12-15',
                        release_date_precision=ReleaseDatePrecision.DAY,
                        uri='spotify:episode:0zLhl3WsOCQHbe1BPTiHgr',
                        available_markets=[
                            'available_markets2'
                        ],
                        resume_point=ResumePointObject(
                            fully_played=False,
                            resume_position_ms=254,
                            additional_properties={
                                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                            }
                        ),
                        restrictions=ChapterRestrictionObject(
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
            edition='Unabridged',
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



