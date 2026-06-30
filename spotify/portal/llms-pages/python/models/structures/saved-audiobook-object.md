# Saved Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlNhdmVkQXVkaW9ib29rT2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`SavedAudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `added_at` | `datetime` | Optional | The date and time the audiobook was saved<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `audiobook` | [`AudiobookObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/audiobook-object.md) | Optional | Information about the audiobook. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.audiobook_object import AudiobookObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.author_object import AuthorObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.chapter_base import ChapterBase
from spotifywebapiwithfixesandimprovementsfromsonallux.models.chapter_restriction_object import ChapterRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.narrator_object import NarratorObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_simplified_chapter_object import PagingSimplifiedChapterObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.resume_point_object import ResumePointObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.saved_audiobook_object import SavedAudiobookObject

saved_audiobook_object = SavedAudiobookObject(
    added_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    audiobook=AudiobookObject(
        authors=[
            AuthorObject(
                name='name0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        available_markets=[
            'available_markets2',
            'available_markets3',
            'available_markets4'
        ],
        copyrights=[
            CopyrightObject(
                text='text2',
                mtype='type2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            CopyrightObject(
                text='text2',
                mtype='type2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
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
                url='url6',
                height=182,
                width=222,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            ImageObject(
                url='url6',
                height=182,
                width=222,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            ImageObject(
                url='url6',
                height=182,
                width=222,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        languages=[
            'languages3',
            'languages4'
        ],
        media_type='media_type4',
        name='name8',
        narrators=[
            NarratorObject(
                name='name0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            NarratorObject(
                name='name0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        publisher='publisher4',
        uri='uri2',
        total_chapters=186,
        chapters=PagingSimplifiedChapterObject(
            href='href4',
            limit=230,
            next='next0',
            offset=122,
            previous='previous0',
            total=136,
            items=[
                ChapterBase(
                    audio_preview_url='audio_preview_url4',
                    chapter_number=164,
                    description='description2',
                    html_description='html_description2',
                    duration_ms=52,
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
                            url='url6',
                            height=182,
                            width=222,
                            additional_properties={
                                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                            }
                        ),
                        ImageObject(
                            url='url6',
                            height=182,
                            width=222,
                            additional_properties={
                                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                            }
                        )
                    ],
                    is_playable=False,
                    languages=[
                        'languages5'
                    ],
                    name='name8',
                    release_date='release_date6',
                    release_date_precision=ReleaseDatePrecision.MONTH,
                    uri='uri2',
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
        edition='edition8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



